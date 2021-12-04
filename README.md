## Wellcome to the porject documentation



### Functions
#### <span style="color:blue">unit_transformation(unit=[0,0,0],bool)</span>

conversion between SI and natural unit, enter the index of [m, hz, eV]. <br>
bool:<br>
-> true: from SI to atomic unit<br>
-> false: from atomic to SI<br>


#### <span style="color:blue">C6_calculation(channel = list, starting_state = list, n_range = int)</span>

Calculate C6 coeffient given channels, starting state and the range of n values.<br>
only focus on nP_{1/2} and nP_{1/2} transitions<br>
The four channels we have are:<br>
<br>
nP_{1/2} + nP_{1/2} to n'S_{1/2} + n''S_{1/2}<br>
nP_{1/2} + nP_{1/2} to n'D_{3/2} + n''D_{3/2}<br>
nP_{1/2} + nP_{1/2} to n'S_{1/2} + n''D_{3/2}<br>
nP_{1/2} + nP_{1/2} to n'D_{3/2} + n''S_{1/2}<br>
<br>




```markdown

```

