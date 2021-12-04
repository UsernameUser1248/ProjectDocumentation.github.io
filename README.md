
<script type="text/javascript" src="http://cdn.mathjax.org/mathjax/latest/MathJax.js?config=default"></script>
## Wellcome to the porject documentation

### Functions
#### <span style="color:blue">unit_transformation(unit=[0,0,0],bool)</span>

conversion between SI and natural unit, enter the index of [m, hz, eV]. <br>
bool:<br>
-> true: from SI to atomic unit<br>
-> false: from atomic to SI<br>


#### <span style="color:blue">C6_calculation(channel = list, starting_state = list, n_range = int)</span>
Get the combined C6 coefficient for all the channels

|n,l,j,n,l,j\rangle \leftrightarrow |n_1,l_1,j_1,n_2,l_2,j_2\rangle 



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
Gives the matrix element of D as in Alex theses.

conversion between SI and natural unit, enter the index of [m, hz, eV]. <br>
bool:<br>
-> true: from SI to atomic unit<br>
-> false: from atomic to SI<br>



```markdown

```

