Download Link: https://assignmentchef.com/product/solved-comp424-artificial-intelligence-homework-3
<br>
<h1>Question 1:  Designing a Bayesian Network</h1>




Marv the cat is having a bad day. His brother Harry ate all the food set out by their owner, Shannon, so Marv has to find a way to feed himself. He can try to catch a fish in the lake outside, and if he succeeds, he’ll eat it. If it’s a hot day, Marv will be sluggish, so he’s less likely to catch a fish. Marv can also try to steal Shannon’s sandwich, which does not depend on the outside temperature. However, even if he succeeds in stealing the sandwich, he might not get to eat it (for example, Shannon may notice and snatch it back). Finally, if Marv manages to eat at least something, he might feel content, in spite of everything. However, if it’s hot out, he is less likely to feel content in general.




Consider the Boolean variables:  H (it’s a hot day), C (Marv is content), E (Marv eats at least one item), F (Marv catches a fish), S (Marv steals the sandwich).




<ol>

 <li>Draw a Bayesian network for this domain. Only include the Boolean variables listed above, so your network should have 5 nodes.</li>

 <li>Is your network a polytree? Why or why not? (NB: a polytree is a graph that has no directed or undirected cycles.)</li>

 <li>Suppose the probability that Marv catches the fish is <em>x</em>​ ​ when it’s hot, and <em>y</em>​ ​ when it is not. Give the conditional probability table associated with F.</li>

 <li>Suppose that if Marv catches a fish, he will eat it with probability 1, and if he successfully steals the sandwich, he will eat it with probability 0.5. If he fails at both hunting and stealing, then he will not eat anything. Give the conditional probability table associated with E.</li>

 <li>Suppose Marv is content. Write down the expression for the probability that it is a hot day, in terms of the various conditional probabilities in the network.</li>

</ol>

<strong> </strong>

<h1>Question 2:  Inference in Bayesian Networks</h1>

Consider the following Bayesian Network




R: rush hour

B: bad weather

A: accident

T: traffic jam

S: sirens
















We denote random variables with capital letters (e.g., R for “rush hour”), and the binary outcomes with lowercase letters (e.g., r and ¬r for “it is rush hour” and “it is not rush hour,” respectively).




The network has the following parameters:




P(b)=0.4

P(r)=0.2




P(t|r, b,a) = 0.98

P(t|r, ¬b,a) = 0.9

P(t|r,b,¬a) = 0.88

P(t|r,¬b,¬a) = 0.85

P(t|¬r,b,a) = 0.5

P(t|¬r,b,¬a) = 0.4

P(t|¬r,¬b,a) = 0.6

P(t|¬r,¬b,¬a) = 0.05




P(s|a) = 0.95

P(s|¬a) = 0.2




P(a|b) = 0.7

P(a|¬b) = 0.2




Compute the following terms using basic axioms of probability and the conditional independence properties encoded in the above graph. a.            P(a, ¬r)

<ol>

 <li>P(b, a)</li>

</ol>




For the query P(b|a):

<ol>

 <li>Use Bayes Ball to determine the set of nodes that can be pruned from the graph.</li>

 <li>Compute P(b|a) using the simplifications determined in Part c.</li>

</ol>

<h1>Question 3:  Variable Elimination</h1>

For the graph above, compute the MAP result of querying P(T|b) using variable elimination with the following order: S, A, R, T.




Clearly explain each step. For each of the intermediate factors created, explain what probabilistic function it represents.

<strong> </strong>

<h1>Question 4:  Learning with Bayesian Networks</h1>

Consider the following Bayesian network. Assume that the variables are distributed according to Bernoulli distributions.










<ol>

 <li>We are given the following dataset with 144 samples, from which we will estimate the parameters of the model.</li>

</ol>




<table width="475">

 <tbody>

  <tr>

   <td width="138"><strong>A </strong></td>

   <td width="95"><strong>B </strong></td>

   <td width="95"><strong>C </strong></td>

   <td width="62"><strong>D </strong></td>

   <td width="85"><strong># Instances </strong></td>

  </tr>

  <tr>

   <td width="138">0</td>

   <td width="95">0</td>

   <td width="95">0</td>

   <td width="62">0</td>

   <td width="85">2</td>

  </tr>

  <tr>

   <td width="138">0</td>

   <td width="95">0</td>

   <td width="95">0</td>

   <td width="62">1</td>

   <td width="85">4</td>

  </tr>

  <tr>

   <td width="138">0</td>

   <td width="95">0</td>

   <td width="95">1</td>

   <td width="62">0</td>

   <td width="85">18</td>

  </tr>

  <tr>

   <td width="138">0</td>

   <td width="95">0</td>

   <td width="95">1</td>

   <td width="62">1</td>

   <td width="85">3</td>

  </tr>

  <tr>

   <td width="138">0</td>

   <td width="95">1</td>

   <td width="95">0</td>

   <td width="62">0</td>

   <td width="85">14</td>

  </tr>

  <tr>

   <td width="138">0</td>

   <td width="95">1</td>

   <td width="95">0</td>

   <td width="62">1</td>

   <td width="85">2</td>

  </tr>

  <tr>

   <td width="138">0</td>

   <td width="95">1</td>

   <td width="95">1</td>

   <td width="62">0</td>

   <td width="85">31</td>

  </tr>

  <tr>

   <td width="138">0</td>

   <td width="95">1</td>

   <td width="95">1</td>

   <td width="62">1</td>

   <td width="85">10</td>

  </tr>

  <tr>

   <td width="138">1</td>

   <td width="95">0</td>

   <td width="95">0</td>

   <td width="62">0</td>

   <td width="85">1</td>

  </tr>

  <tr>

   <td width="138">1</td>

   <td width="95">0</td>

   <td width="95">0</td>

   <td width="62">1</td>

   <td width="85">0</td>

  </tr>

  <tr>

   <td width="138">1</td>

   <td width="95">0</td>

   <td width="95">1</td>

   <td width="62">0</td>

   <td width="85">3</td>

  </tr>

  <tr>

   <td width="138">1</td>

   <td width="95">0</td>

   <td width="95">1</td>

   <td width="62">1</td>

   <td width="85">23</td>

  </tr>

  <tr>

   <td width="138">1</td>

   <td width="95">1</td>

   <td width="95">0</td>

   <td width="62">0</td>

   <td width="85">0</td>

  </tr>

  <tr>

   <td width="138">1</td>

   <td width="95">1</td>

   <td width="95">0</td>

   <td width="62">1</td>

   <td width="85">9</td>

  </tr>

  <tr>

   <td width="138">1</td>

   <td width="95">1</td>

   <td width="95">1</td>

   <td width="62">0</td>

   <td width="85">14</td>

  </tr>

  <tr>

   <td width="138">1</td>

   <td width="95">1</td>

   <td width="95">1</td>

   <td width="62">1</td>

   <td width="85">10</td>

  </tr>

 </tbody>

</table>




<ol>

 <li>Enumerate the parameters that must be learned. Specify the parameter name and the probability that it represents (i.e., for each parameter, write something in the form, θ<em><sub>X </sub></em>= <em>Pr </em>(<em>X</em>).</li>

 <li>Give the maximum likelihood estimate for each parameter.</li>

</ol>

<ul>

 <li>Give the maximum <em>a posteriori</em>​ ​ (MAP) estimate for each parameter after applying Laplace smoothing.</li>

</ul>







<ol>

 <li>Assume that in addition to the data in the table above, you are given the following incomplete data instances:</li>

</ol>

<strong>A B C D </strong>S1 1 ? 1 ?

S2              1          1          0          0




We will apply the (soft) EM algorithm on these instances. Initialize the model using your parameter estimates from Part a., Subpart ii. (i.e., use the MLE).




<ol>

 <li>Show the computation of the first E-step, providing the weights for each possible assignment of the incomplete data for each sample.</li>

 <li>What are the parameters obtained for the first M-step? Weight each of the samples from the original dataset and the two new samples equally (i.e., you now have 146 samples).</li>

</ol>

<ul>

 <li>Show the computation of the second E-step.</li>

</ul>























