
https://usernameuser1248.github.io/ProjectDocumentation.github.io/
## Wellcome to the porject documentation

### Functions
#### <span style="color:blue">unit_transformation(unit=[0,0,0],bool)</span>

conversion between SI and natural unit, enter the index of [m, hz, eV]. <br>
bool:<br>
-> true: from SI to atomic unit<br>
-> false: from atomic to SI<br>


#### <span style="color:blue">C6_calculation(channel = list, starting_state = list, n_range = int)</span>
Get the combined C6 coefficient for all the channels

[n,l,j,n,l,j>  ->  [n_1,l_1,j_1,n_2,l_2,j_2>

channels:[[l_1, j_1], [l_2, j_2]]<br>
Starting_state would be in the form of [n,l,j]<br>
n_range=\delta_n <br>

only focus on nP_{1/2} and nP_{1/2} transitions<br>
The four channels we have are:<br>
<br>

nP_{1/2} + nP_{1/2} to n'S_{1/2} + n''S_{1/2}<br>
nP_{1/2} + nP_{1/2} to n'D_{3/2} + n''D_{3/2}<br>
nP_{1/2} + nP_{1/2} to n'S_{1/2} + n''D_{3/2}<br>
nP_{1/2} + nP_{1/2} to n'D_{3/2} + n''S_{1/2}<br>

<br>

#### <span style="color:blue">matrix_element_calculation(bra_state = list, ket_state = list, theta = float, phi = float):</span>
Calculates the matrix <l1,j1,m1;l2,j2,m2|M|la,ja,ma;lb,jb,mb><br>
The formula for this expression is given in the Alex theses.<br>


#### <span style="color:blue">state_couple(initial_state = list, final_state = list, channel = list, theta = float, phi = float):</span>
Gives the matrix element of D as in Alex theses.<br>
initial_state is a list with [[l_1,j_1,m_1], [l_2,j_2,m_2]]<br>
final_state is a list with [[l_3,j_3,m_3], [l_4,j_4,m_4]]<br>
channel is a list with [[l_alpha, j_alpha],[l_beta, j_beta]], the intermediate states.<br>

    
#### <span style="color:blue">full_matrix(state = list, channel = list, theta = float, phi = float):</span>
Gives the matrix D as in Alex theses.<br>
state is a list with [[l_1,j_1],[l_2,j_2]]<br>
channel is a list with [[l_alpha, j_alpha],[l_beta, j_beta]], the intermediate states.<br>
size of the matrix is determined by j values.<br>

#### <span style="color:blue">H_vdw(states = list, channels = list, n_range = float, theta = float, phi = float):</span>
Calculates H_vdw.<br>
states are lists that contain [ [n_1,l_1,j_1],[n_2,l_2,j_2] ]<br>
Channels are list of [channel_a, Channel_b, Channel_c,...]<br>
each channel is [[l_alpha,j_alpha],[l_beta,j_beta]]<br>
n_range is for C6 calculation to specify what the range of n we want to run through theta and phi are the angles<br>

#### <span style="color:blue">Van_der_Waals(states = list, channels = list, n_range = float, theta = float, phi = float, distance = float):</span>
Calculates V++, V+-, W++, W+- terms.<br>
outputlist = [V_pp, V_pm, W_pm, W_pp]<br>

#### <span style="color:blue">Energy_eigenstate(energy_levels = list, delta_p = float, delta_m = float):</span>
Defined the eigenenergies accroding to Alex theses.<br>
The energy levels should be expressed as [V_pp,V_pm,W_pm.W_pp]<br>
the output would be a list which is [E_pp,E_pm,E_mp,E_mm]<br>
return [E_pp,E_pm,E_mp,E_mm]<br>

#### <span style="color:blue">effective_vdw(van_der_waals_energy = list, Omega = list, detuning = list):</span>
Defined the effective hamiltonian accroding to Alex theses.<br>
van_der_waals_energy is the energy level that we construct without the laser detuning<br>
van_der_waals_energy = [V_pp, V_pm, W_pm, W_pp],<br>
directly use the result from Van_der_Waals.<br>
Omega is the laser strength, it is in the form [Omega_p, Omega_m]<br>
Detuning is the laser detuning, it is in the form [delta_p. delta_m]<br>
return [V_tilda_pp, V_tilda_mm, W_tilda_pp, V_tilda_pm, W_tilda_pm].<br>


#### <span style="color:blue">asymptotic_energy(Omega = list, detuning = list):</span>
Defined accroding to Alex theses.<br>
output_list = [V_asymptotic_pp, V_asymptotic_mm, V_asymptotic_pm]<br>

#### <span style="color:blue">spin_interaction(effective_vdw = list):</span>
Defined J accroding to Alex theses using effective_vdw.<br>
output_list = [J_parallel,J_z,J_pm,J_pp]<br>
