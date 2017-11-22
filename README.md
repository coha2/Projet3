%%# Projet3
%% Projet3 gestion de production
% Script general 

%% 1 synthese et separation du NH3 
% 3H2 + N2 <-> 2NH3 [a, b, c] sont les quantites de moles des differents
% composants 
p1 =  % pression [bar]
T1 =   % Temperature [K]
a1 = 125*10^6  ; 
b1 = (125*10^6/3) *0.99 ; 
c1 = 0 ; 
K1 =  1.665*10^(-5) ; 
% calcul 
[w1 x1 y1] = synthese(a1, b1, c1, T1, p1) ; 

%% 2 separation du CO2 
p2 =  % pression [bar]
T2 =   % Temperature [K]
a2 = 125*10^6  ; 
b2 = 125*10^6 ; 
c2 = 0 ; 
d2 = 0; 
K2 =  0; 



%% 3 Water Gas shift 
% % CO + H2O -> CO2 + H2 [a, b, c, d] sont les quantites de moles des differents
% composants 
p3 =  % pression [bar]
T3 =   % Temperature [K]
a3 = 3*a1/(3*x1 + x2+5) + exces   ; 
b3 = 3*a1/(3*x1 + x2+5) ; 
c3 = 3*a1/(3*x1 + x2+5) ; 
d3 = 3*a1/(3*x1 + x2+5) ;
K3 =  0 ; 
% calcul 
%[w3 x3 y3 z3] = synthese(a1, b1, c1, d1, T1, p1) 


%% 4 reformage secondaire 
% 2CH4 + O2 -> 4H2 + 2CO 
[a, b, c, d] sont les quantites de moles des differents
% composants 
p4 =  % pression [bar]
T4 =   % Temperature [K]
n4 = 4*3*a1/(3*x1 + x2+5) ; 
a4 = n4*2 ;
b4 = n4; 
c4 = 4*n4 ; 
d4 = 2*n4;
K4 =  0 ; 
% calcul 
%[w4 x4 y4 z4] = reformageSecondaire(a4, b4, c4, d4, T4, p4) 


%% 5 reformage primaire 
% CH4 + H20 <-> CO + 3H2 [a b c d]
% CO + H2O <-> CO2 + H2 [c b e d]
T5 = 725 ;
p5 = 30 ; 
n5 = 3*3*125*(10^6)/(5+3*x1 + x2) ; 
a5 = (1-x1)*n5;
b5 = (1-x1-x2)*n5 ; 
c5 = (x1-x2)*n5 ;
d5 = n5 ; 
e5 = x2*n5 ; 
K5_1 =
K5_2 =



%% 6 four 
DeltaT = 0; 




