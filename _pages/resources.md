---
layout: archive
title: "Useful Open Source Materials"
permalink: /resources/
author_profile: true
---

Here are some open-source materials that may be useful for researchers in computational geomechanics.
 
- Applied Mechanics of Solids by Prof. Allan F. Bower of Brown University \[[Link](http://solidmechanics.org/)\]
- Continuum Mechanics Notes of MIT \[[Link](https://web.mit.edu/abeyaratne/Volumes/RCA_Vol_II.pdf)\]
- Nonlinear Solid Mechanics for Finite Element Analysis \[[FLagSHyP](http://www.flagshyp.com/)\] \[[Penn State](https://github.com/rhk12/flagshyp)\]
- Phase-field model open source code by Prof. Emilio Martínez Pañeda​ of Imperial College London \[[Link](https://www.empaneda.com/codes/)\]
- GitHub repository on poromechanics \[[Two-phase flow](https://github.com/Sbai7/TwoPhasesParticleTransport)\] \[[GeoMatFEM](https://github.com/nicolospiezia/GeoMatFEM)\] \[[FVBiot](https://github.com/keileg/fvbiot)\] \[[PorePy](https://github.com/pmgbergen/porepy#porepy-a-simulation-tool-for-fractured-and-deformable-porous-media-written-in-python)\] \[[Porous Media Group](https://github.com/pmgbergen)\]
- Poromechanics educational resources authored by the EMI poromechanics committee \[[Link](https://emi-poromechanics.github.io/)\]
- Multi-physics numerical simulator for MHBS by 青岛海洋地质研究所 Prof. Yizhao Wan \[[QIMGHyd](https://gitee.com/wanyzh/qimghyd-thmc)\]
- \[[PhiPsi](http://phipsi.top/)\]


Occasionally, I will also upload and share some of my notes of mathematical derivations or useful code snippets.

- Here is the MATLAB code for anisotropic elasticity (fourth-order elastic moduli tensor, 9\*9 matrix form, Voigt notation 6\*6 matri form, etc.) The theory could be found in this [[PDF]](../files/anisotropic_elasticity.txt){:target="_blank"}

```MATLAB
clear; clearvars -global; clc; close all;
restoredefaultpath;
rng('default');
format short

Ev = 20;
Eh = 40;
nuhh = 0.2;
nuvh = 0.25;
Gvh = 15;

% Ev = 20;
% Eh = 20;
% nuhh = 0.2;
% nuvh = 0.2;
% Gvh = Eh/2/(1+nuhh);

S11 = [1/Eh, -nuhh/Eh, -nuvh/Ev; ...
    -nuhh/Eh, 1/Eh, -nuvh/Ev; ...
    -nuvh/Ev, -nuvh/Ev, 1/Ev];
S = [S11,zeros(3,3);zeros(3,3),diag([2*(1+nuhh)/Eh, 1/Gvh, 1/Gvh])]; % Compliance matrix 6*6 (VTI)
C = S\eye(6); % Stiffness matrix 6*6 (VTI)

lambda = C(1,2); mu_T = C(4,4); mu_L = C(5,5);
alpha = C(1,3)-C(1,2); beta = C(3,3) - lambda - 4*mu_L + 2*mu_T - 2*alpha; % Same unit as Ev/Eh/Gvh for these 5 constants

I2 = eye(3); % Second order identity tensor
I4 = zeros(3,3,3,3); % Fourth order identity tensor
Ce = zeros(3,3,3,3); % Stiffness 4th-order tensor (general case, not necessarily VTI)

n = [sqrt(1/6); sqrt(2/6); sqrt(3/6)];

m = n*n';
for i = 1:3
    for j = 1:3
        for k = 1:3
            for l = 1:3
                I4(i, j, k, l) = (i==k)*(j==l);
                Ce(i, j, k, l) = lambda*(i==j)*(k==l) + 2*mu_T*I4(i, j, k, l) ...
                    + alpha*((i==j)*m(k, l) + m(i, j)*(k==l)) + beta*(m(i, j)*m(k, l)) ...
                    + 2*(mu_L - mu_T)*(m(i, k)*(j==l) + (i==k)*m(j, l));
            end
        end
    end
end
clearvars i j k l

% Define a rotation
Q = rotz(180); % rotx(deg), roty(deg)
e = randn(3,3); e = (e + e')/2;
RHS = Q*double_dot(Ce, e)*Q';
LHS = double_dot(Ce, Q*e*Q');

disp(stiffness_to_mat6by6(Ce));

Ce2 = zeros(3,3,3,3);
for i = 1:3
    for j = 1:3
        for k = 1:3
            for l = 1:3
                for a = 1:3
                    for b = 1:3
                        for c = 1:3
                            for d = 1:3
                                Ce2(i,j,k,l) = Ce2(i,j,k,l) + Q(i,a)*Q(j,b)*Q(k,c)*Q(l,d)*Ce(a,b,c,d);
                            end
                        end
                    end
                end
            end
        end
    end
end
clearvars i j k l a b c d

disp(stiffness_to_mat6by6(Ce2) - stiffness_to_mat6by6(Ce));

E = zeros(9,6); E(1,1) = 1; E(5, 2) = 1; E(9, 3) = 1; E(2, 4) = 0.5; E(4, 4) = 0.5; E(3, 5) = 0.5; E(7, 5) = 0.5; E(6, 6) = 0.5; E(8, 6) = 0.5;
index = [1, 5, 9, 4, 7, 8];

DELAS = reshape(Ce, [9,9])*E; % The use of reshape here is correct! (Specific transformation rule (instead of the Voigt notation, use full matrix/vector version)!)
DELAS = DELAS(index, :);  % 6*6 matrix
disp(DELAS - stiffness_to_mat6by6(Ce));
```

```MATLAB
function B = stiffness_to_mat6by6(A)
% Transform a symmetric (minor and major) fourth order tensor A (3*3*3*3) to a matrix B (6*6)
% Only apply to stiffness!
% Note Voigt order: 11 22 33 12 13 23 is used here

e1 = [1, 0, 0; 0, 0, 0; 0, 0, 0];
e2 = [0, 0, 0; 0, 1, 0; 0, 0, 0];
e3 = [0, 0, 0; 0, 0, 0; 0, 0, 1];
e4 = [0, 0.5, 0; 0.5, 0, 0; 0, 0, 0];
e5 = [0, 0, 0.5; 0, 0, 0; 0.5, 0, 0];
e6 = [0, 0, 0; 0, 0, 0.5; 0, 0.5, 0];

D_aug = [reshape(double_dot(A, e1), [9, 1]), reshape(double_dot(A, e2), [9, 1]), ...
    reshape(double_dot(A, e3), [9, 1]), reshape(double_dot(A, e4), [9, 1]),...
    reshape(double_dot(A, e5), [9, 1]), reshape(double_dot(A, e6), [9, 1])]; % 9*6 matrix

B = [D_aug(1,:); D_aug(5,:); D_aug(9,:); D_aug(4,:); D_aug(7,:); D_aug(8,:)];
end
```


```MATLAB
function C = double_dot(A,B)
% double contraction between tensors
m = size(A); m(end-1:end) = [];
n = size(B); n(1:2) = [];

if length(m) == 2 && length(n) == 2
    for i = 1:3
        for j = 1:3
            for k = 1:3
                for l = 1:3
                    C(i, j, k, l) = trace(reshape(A(i, j, :, :), [3, 3]) * B(:, :, k, l)');
                end
            end
        end
    end
elseif length(m) == 2 && isempty(n)
    for i = 1:3
        for j = 1:3
            C(i, j) = trace(reshape(A(i, j, :, :), [3, 3]) * B');
        end
    end
elseif length(n) == 2 && isempty(m)
    for i = 1:3
        for j = 1:3
            C(i, j) = trace(A* transpose(reshape(B(:, :, i, j), [3, 3])));
        end
    end
elseif isempty(m) && isempty(n)
    C = trace(A*B');
end                  

end

```