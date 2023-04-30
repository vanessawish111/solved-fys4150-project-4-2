Download Link: https://assignmentchef.com/product/solved-fys4150-project-4-2
<br>



<h1>Studies of phase transitions in magnetic systems</h1>

<strong>Introduction. </strong>The aim of this project is to study a widely popular model to simulate phase transitions, the so-called Ising model in two dimensions. At a given critical temperature, this model exhbits a phase transition from a magnetic phase (a system with a finite magnetic moment) to a phase with zero magnetization. This is a so-called binary system where the objects at each lattice site can only take two values. These could be 0 and 1 or other values. Here we will use spins pointing up or down as the model for our system. But we could replace the spins with blue and green balls for example. The <a href="https://en.wikipedia.org/wiki/Ising_model">Ising </a><a href="https://en.wikipedia.org/wiki/Ising_model">model</a> has been extremely popular, with applications spanning from studies of phase transitions to simulations in statistics. In one and two dimensions its has analytical solutions to several expectation values and it gives a qualitatively good underatanding of several types of phase transitions.

In its simplest form the energy of the Ising model is expressed as, without an externally applied magnetic field,

<em>N</em>

<em>E </em>= <em>−J </em><sup>X </sup><em>s<sub>k</sub>s<sub>l</sub></em>

<em>&lt;kl&gt;</em>

with <em>s<sub>k </sub></em>= <em>±</em>1. The quantity <em>N </em>represents the total number of spins and <em>J </em>is a coupling constant expressing the strength of the interaction between neighboring spins. The symbol <em>&lt; kl &gt; </em>indicates that we sum over nearest neighbors only. We will assume that we have a ferromagnetic ordering, viz <em>J &gt; </em>0. We will use periodic boundary conditions and the Metropolis algorithm only. The material on the Ising model can be found in chapter 13 of the lecture notes. The Metropolis algorithm is discussed in chapter 12.

<strong>For this project you can hand in collaborative reports and programs. </strong>This project (together with projects 3 and 5) counts 1/3 of the final mark.

<em> </em>c 1999-2019, “Computational Physics I

FYS3150/FYS4150″:”http://www.uio.no/studier/emner/matnat/fys/FYS3150/indexeng.html”. Released under CC Attribution-NonCommercial 4.0

license

<strong>Project 4a): A simple </strong>2 <em>× </em>2 <strong>lattice, analytical expressions. </strong>Assume we have only two spins in each dimension, that is <em>L </em>= 2. Find the analytical expression for the partition function and the corresponding expectations values for the energy <em>E</em>, the mean absolute value of the magnetic moment <em>|M| </em>(we will refer to this as the mean magnetization), the specific heat <em>C<sub>V </sub></em>and the susceptibility <em>χ </em>as functions of <em>T </em>using periodic boundary conditions. These results will serve as benchmark calculations for our next steps.

<strong>Project 4b): Writing a code for the Ising model. </strong>Write now a code for the Ising model which computes the mean energy <em>E</em>, mean magnetization <em>|M|</em>, the specific heat <em>C<sub>V </sub></em>and the susceptibility <em>χ </em>as functions of <em>T </em>using periodic boundary conditions for <em>L </em>= 2 in the <em>x </em>and <em>y </em>directions. Compare your results with the expressions from a) for a temperature <em>T </em>= 1<em>.</em>0 (in units of <em>kT/J</em>).

How many Monte Carlo cycles do you need in order to achieve a good agreeement?

<strong>Project 4c): When is the most likely state reached? </strong>We choose now a square lattice with <em>L </em>= 20 spins in the <em>x </em>and <em>y </em>directions.

In the previous exercise we did not study carefully how many Monte Carlo cycles were needed in order to reach the most likely state. Here we want to perform a study of the time (here it corresponds to the number of Monte Carlo sweeps of the lattice) one needs before one reaches an equilibrium situation and can start computing various expectations values. Our first attempt is a rough and plain graphical one, where we plot various expectations values as functions of the number of Monte Carlo cycles.

Choose first a temperature of <em>T </em>= 1<em>.</em>0 (in units of <em>kT/J</em>) and study the mean energy and magnetisation (absolute value) as functions of the number of Monte Carlo cycles. Let the number of Monte Carlo cycles (sweeps per lattice) represent time. Use both an ordered (all spins pointing in one direction) and a random spin orientation as starting configuration. How many Monte Carlo cycles do you need before you reach an equilibrium situation? Repeat this analysis for <em>T </em>= 2<em>.</em>4. Can you, based on these values estimate an equilibration time? Make also a plot of the total number of accepted configurations as function of the total number of Monte Carlo cycles. How does the number of accepted configurations behave as function of temperature <em>T</em>?

<strong>Project 4d): Analyzing the probability distribution. </strong>Compute thereafter the probability <em>P</em>(<em>E</em>) for the previous system with <em>L </em>= 20 and the same temperatures, that is at <em>T </em>= 1<em>.</em>0 and <em>T </em>= 2<em>.</em>4. You compute this probability by simply counting the number of times a given energy appears in your computation. Start the computation after the steady state situation has been reached. Compare your results with the computed variance in energy <em>σ<sub>E</sub></em><sup>2 </sup>and discuss the behavior you observe.

<strong>Studies of phase transitions.            </strong>Near <em>T<sub>C </sub></em>we can characterize the behavior of many physical quantities by a power law behavior. As an example, for the Ising class of models, the mean magnetization is given by

<em>hM</em>(<em>T</em>)<em>i ∼ </em>(<em>T − T<sub>C</sub></em>)<em><sup>β </sup>,</em>

where <em>β </em>= 1<em>/</em>8 is a so-called critical exponent. A similar relation applies to the heat capacity

<em>C<sub>V </sub></em>(<em>T</em>) <em>∼ |T<sub>C </sub>− T</em><em><sup>|α </sup>,</em>

and the susceptibility

<em>χ</em>(<em>T</em>) <em>∼ |T<sub>C </sub>− T|<sup>γ </sup>,                                                         </em>(1)

with <em>α </em>= 0 and <em>γ </em>= 7<em>/</em>4. Another important quantity is the correlation length, which is expected to be of the order of the lattice spacing for <em>T &gt;&gt; T<sub>C</sub></em>. Because the spins become more and more correlated as <em>T </em>approaches <em>T<sub>C</sub></em>, the correlation length increases as we get closer to the critical temperature. The divergent behavior of <em>ξ </em>near <em>T<sub>C </sub></em>is

<em>ξ</em>(<em>T</em>) <em>∼ |T<sub>C </sub>− T|<sup>−ν </sup>.                                                        </em>(2)

A second-order phase transition is characterized by a correlation length which spans the whole system. Since we are always limited to a finite lattice, <em>ξ </em>will be proportional with the size of the lattice. Through so-called finite size scaling relations it is possible to relate the behavior at finite lattices with the results for an infinitely large lattice. The critical temperature scales then as

<em>T<sub>C</sub></em>(<em>L</em>) <em>− T<sub>C</sub></em>(<em>L </em>= <em>∞</em>) = <em>aL<sup>−</sup></em><sup>1<em>/ν</em></sup><em>,                                                 </em>(3)

with <em>a </em>a constant and <em>ν </em>defined in Eq. (2). We set <em>T </em>= <em>T<sub>C </sub></em>and obtain a mean magnetisation

<em>hM</em>(<em>T</em>)<em>i ∼ </em>(<em>T − T<sub>C</sub></em>)<em><sup>β </sup>→ L<sup>−β/ν</sup>,                                                </em>(4)

a heat capacity

<em>C<sub>V </sub></em>(<em>T</em>) <em>∼ |T<sub>C </sub>− T|<sup>−γ </sup>→ L<sup>α/ν</sup>,                                                 </em>(5)

and susceptibility

<em>χ</em>(<em>T</em>) <em>∼ |T<sub>C </sub>− T|<sup>−α </sup>→ L<sup>γ/ν</sup>.                                                   </em>(6)

<strong>Project 4e): Numerical studies of phase transitions. </strong>We wish to study the behavior of the Ising model in two dimensions close to the critical temperature as a function of the lattice size <em>L × L</em>. Calculate the expectation values for <em>hEi </em>and <em>h|M|i</em>, the specific heat <em>C<sub>V </sub></em>and the susceptibility <em>χ </em>as functions of <em>T </em>for <em>L </em>= 40, <em>L </em>= 60, <em>L </em>= 80 and <em>L </em>= 100 for <em>T ∈ </em>[2<em>.</em>0<em>,</em>2<em>.</em>3] with a step in temperature ∆<em>T </em>= 0<em>.</em>05 or smaller. You may find it convenient to narrow the domain for <em>T</em>.

Plot <em>hEi</em>, <em>h|M|i</em>, <em>C<sub>V </sub></em>and <em>χ </em>as functions of <em>T</em>. Can you see an indication of a phase transition? Use the absolute value <em>h|M|i </em>when you evaluate <em>χ</em>. For these production runs you should parallelize the code using MPI (recommended). Alternatively OpenMP can be used. Use optimization flags when compiling. Perform a timing analysis of some selected runs in order to see that you get an optimal speedup when parallelizing your code.

<strong>Project 4f): Extracting the critical temperature. </strong>Use Eq. (3) and the exact result <em>ν </em>= 1 in order to estimate <em>T<sub>C </sub></em>in the thermodynamic limit <em>L → ∞ </em>using your simulations with <em>L </em>= 40, <em>L </em>= 60, <em>L </em>= 80 and <em>L </em>= 100 The exact result<em>√</em>

for the critical temperature (<a href="https://journals.aps.org/pr/abstract/10.1103/PhysRev.65.117">after Lars Onsager</a><a href="https://journals.aps.org/pr/abstract/10.1103/PhysRev.65.117">)</a> is <em>kT<sub>C</sub>/J </em>= 2<em>/ln</em>(1+ 2) <em>≈ </em>2<em>.</em>269 with <em>ν </em>= 1.

<h1>Background literature</h1>

If you wish to read more about the Ising model and statistical physics here are three suggestions.

<ul>

 <li><a href="http://www.worldscientific.com/worldscibooks/10.1142/5660"> Plischke and B. Bergersen</a><a href="http://www.worldscientific.com/worldscibooks/10.1142/5660">,</a> <em>Equilibrium Statistical Physics</em>, World Scientific, see chapters 5 and 6.</li>

 <li><a href="https://www.cambridge.org/no/academic/subjects/physics/computational-science-and-modelling/guide-monte-carlo-simulations-statistical-physics-4th-edition?format=HB"> P. Landau and K. Binder</a><a href="https://www.cambridge.org/no/academic/subjects/physics/computational-science-and-modelling/guide-monte-carlo-simulations-statistical-physics-4th-edition?format=HB">,</a> <em>A Guide to Monte Carlo Simulations in Statistical Physics</em>, Cambridge, see chapters 2,3 and 4.</li>

 <li><a href="https://global.oup.com/academic/product/monte-carlo-methods-in-statistical-physics-9780198517979?cc=no&amp;lang=en&amp;"> E. J. Newman and T. Barkema</a><a href="https://global.oup.com/academic/product/monte-carlo-methods-in-statistical-physics-9780198517979?cc=no&amp;lang=en&amp;">,</a> <em>Monte Carlo Methods in Statistical Physics</em>, Oxford, see chapters 3 and 4.</li>

</ul>

<h1>Introduction to numerical projects</h1>

Here follows a brief recipe and recommendation on how to write a report for each project.

<ul>

 <li>Give a short description of the nature of the problem and the eventual numerical methods you have used.</li>

 <li>Describe the algorithm you have used and/or developed. Here you may find it convenient to use pseudocoding. In many cases you can describe the algorithm in the program itself.</li>

 <li>Include the source code of your program. Comment your program properly.</li>

 <li>If possible, try to find analytic solutions, or known limits in order to test your program when developing the code.</li>

 <li>Include your results either in figure form or in a table. Remember to label your results. All tables and figures should have relevant captions and labels on the axes.</li>

 <li>Try to evaluate the reliabilty and numerical stability/precision of your results. If possible, include a qualitative and/or quantitative discussion of the numerical stability, eventual loss of precision etc.</li>

 <li>Try to give an interpretation of you results in your answers to the problems.</li>

 <li>Critique: if possible include your comments and reflections about the exercise, whether you felt you learnt something, ideas for improvements and other thoughts you’ve made when solving the exercise. We wish to keep this course at the interactive level and your comments can help us improve it.</li>

 <li>Try to establish a practice where you log your work at the computerlab. You may find such a logbook very handy at later stages in your work, especially when you don’t properly remember what a previous test version of your program did. Here you could also record the time spent on solving the exercise, various algorithms you may have tested or other topics which you feel worthy of mentioning.</li>

</ul>

<h1>Format for electronic delivery of report and programs</h1>

The preferred format for the report is a PDF file. You can also use DOC or postscript formats or as an ipython notebook file. As programming language we prefer that you choose between C/C++, Fortran2008 or Python. The following prescription should be followed when preparing the report:

<ul>

 <li>Use Devilry to hand in your projects, log in at <a href="http://devilry.ifi.uio.no/">http://devilry.ifi. </a><a href="http://devilry.ifi.uio.no/">no</a> with your normal UiO username and password and choose either</li>

</ul>

’fys3150’ or ’fys4150’. There you can load up the files within the deadline.

<ul>

 <li>Upload <strong>only </strong>the report file! For the source code file(s) you have developed please provide us with your link to your github domain. The report file should include all of your discussions and a list of the codes you have developed. Do not include library files which are available at the course homepage, unless you have made specific changes to them.</li>

 <li>In your git repository, please include a folder which contains selected results. These can be in the form of output from your code for a selected set of runs and input parametxers.</li>

 <li>In this and all later projects, you should include tests (for example unit tests) of your code(s).</li>

 <li>Comments from us on your projects, approval or not, corrections to be made etc can be found under your Devilry domain and are only visible to you and the teachers of the course.</li>

</ul>

Finally, we encourage you to work two and two together. Optimal working groups consist of 2-3 students.

<h1>How to install openmpi and/or OpenMP on your PC/laptop</h1>

If you use your own laptop, for linux/ubuntu users, you need to install two packages (alternatively use the synaptic package manager)

sudo apt-get install libopenmpi-dev sudo apt-get install openmpi-bin

For OS X users, install brew (after having installed xcode and gcc, needed for the gfortran compiler of openmpi) and then run brew install open-mpi

When compiling from the command line, depending on your choice of programming language you need to compile and link as for example mpic++ -O3 -o &lt;executable&gt; &lt;programname.cpp&gt; if you use c++ (alternatively mpicxx) and mpif90 -O3 -o &lt;executable&gt; &lt;programname.f90&gt; if you use Fortran90.

When running an executable, run as mpirun -n 10 ./&lt;executable&gt; where -n indicates the number of processes, 10 here.

With openmpi installed, when using Qt, add to your .pro file the instructions at <a href="http://dragly.org/2012/03/14/developing-mpi-applications-in-qt-creator/">Svenn-Arne Dragly’s site</a>

You may need to tell Qt where opempi is stored.

For the machines at the computer lab, openmpi is located at /usr/lib64/openmpi/bin Add to your .bashrc file the following export PATH=/usr/lib64/openmpi/bin:$PATH

For Windows users we recommend to follow the instructions at the <a href="https://www.open-mpi.org/software/ompi/v1.6/ms-windows.php">Open MPI </a><a href="https://www.open-mpi.org/software/ompi/v1.6/ms-windows.php">site</a><a href="https://www.open-mpi.org/software/ompi/v1.6/ms-windows.php">.</a>

If you use OpenMP, for linux users, compile and link with for example c++ -O3 -fopenmp -o &lt;executable&gt; &lt;programname.cpp&gt; For OS X users, you need to install libomp using brew, that is brew install clang-omp and then compile and link with for example c++ -O3 -lomp -o &lt;executable&gt; &lt;programname.cpp&gt;

If you program in Fortran and use <strong>gfortran</strong>, compile as for example gfortran -O3 -fopenmp -o &lt;executable&gt; &lt;programname.f90&gt; If you have access to Intel’s <strong>ifort </strong>compiler, compile as ifort -O3 -fopenmp -o &lt;executable&gt; &lt;programname.f90&gt;