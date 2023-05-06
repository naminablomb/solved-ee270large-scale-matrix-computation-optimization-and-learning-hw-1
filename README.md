Download Link: https://assignmentchef.com/product/solved-ee270large-scale-matrix-computation-optimization-and-learning-hw-1
<br>



<h1>1. Linear Algebra</h1>

Are the following statements <strong>true </strong>or <strong>false</strong>? If true, prove it; if false, show a counterexample.

(a) The inverse of a symmetric matrix is itself symmetric. (b) All 2 × 2 orthogonal matrices have the following form

.

(c) Let can be written as <em>A </em>= <em>CC<sup>T </sup></em>for some matrix <em>C</em>.

<h1>2. Divide and Conquer Matrix Multiplication</h1>

If <em>A </em>is a matrix, then <em>A</em><sup>2 </sup>= <em>AA </em>is the square of <em>A</em>.

<ul>

 <li>Show that five multiplications are sufficient to compute the square of a 2 × 2 matrix</li>

</ul>

, where <em>a</em><sub>1</sub><em>,a</em><sub>2</sub><em>,a</em><sub>3</sub><em>,a</em><sub>4 </sub>are scalars.

<ul>

 <li>Generalize the formula in part (a) to a 2 × 2 block matrix where</li>

</ul>

<em>A</em><sub>1</sub><em>,A</em><sub>2</sub><em>,A</em><sub>3</sub><em>,A</em><sub>4 </sub>are arbitrary matrices.

<ul>

 <li>Instead of using the classical matrix multiplication (three-loop) algorithm for computing <em>A</em><sup>2</sup>, we may apply the block formula you derived in (b) to reduce 2<em>n </em>× 2<em>n </em>problems to several <em>n </em>× <em>n </em>computations, which can be tackled with classical matrix multiplication. Compare the total number of arithmetic operations. Generate 2<em>n</em>×2<em>n </em>random <em>A </em>matrices and plot the wall-clock time of the classical matrix multiplication algorithm and the algorithm using the formula in (b) to compute <em>A</em><sup>2 </sup>for <em>n </em>= 4<em>,…,</em>10000 (or as large as your system memory allows). You can use standard packages for matrix multiplication, e.g., numpy.matmul.</li>

 <li>Show that if you have an algorithm for squaring an <em>n</em>×<em>n </em>matrix in <em>O</em>(<em>n<sup>c</sup></em>) time, then you can use it to multiply any two arbitrary <em>n </em>× <em>n </em>matrices in <em>O</em>(<em>n<sup>c</sup></em>) time. [Hint: Consider multiplying two matrices <em>A </em>and <em>B</em>. Can you define a matrix whose square contains <em>AB</em>?] 3. <strong>Probability (30 pts)</strong></li>

 <li>Random variables <em>X </em>and <em>Y </em>have a joint distribution <em>p</em>(<em>x,y</em>). Prove the following results. You can assume continuous distributions for simplicity.

  <ol>

   <li>E[<em>X</em>] = E<em>Y </em>[E<em>X</em>[<em>X</em>|<em>Y </em>]]</li>

   <li>E[<em>I</em>[<em>X </em>∈ C]] = <em>P</em>(<em>X </em>∈ C), where <em>I</em>[<em>X </em>∈ C] is the indicator function<a href="#_ftn1" name="_ftnref1"><sup>[1]</sup></a> of an arbitrary set C.</li>

  </ol></li>

</ul>

<ul>

 <li>var[X] = E<em>Y </em>[var<em><sub>X</sub></em>[<em>X</em>|<em>Y </em>]] + var<em><sub>Y </sub></em>[E<em>X</em>[<em>X</em>|<em>Y </em>]] iv. If X and Y are independent, then E[<em>XY </em>] = E[<em>X</em>]E[<em>Y </em>].</li>

</ul>

<ol>

 <li>If <em>X </em>and <em>Y </em>take values in {0<em>,</em>1} and E[<em>XY </em>] = E[<em>X</em>]E[<em>Y </em>], then <em>X </em>and <em>Y </em>are independent.</li>

</ol>

<ul>

 <li>Show that the approximate randomized counting algorithm described in Lemma 1 of Lecture 2 slides (page 14) is unbiased:</li>

</ul>

E<em>n</em>˜ = <em>n.                                                                                         </em>(1)

<ul>

 <li>Prove the variance formula in Lemma 2 of Lecture 2 slides (page 38) for Approximate Matrix Multiplication <em>AB </em>≈ <em>CR</em></li>

</ul>

<em>.                                               </em>(2)

where {<em>p<sub>k</sub></em>}<em><sup>d</sup><sub>k</sub></em><sub>=1 </sub>are sampling probabilities.

<h1>4. Positive (Semi-)Definite Matrices</h1>

Let <em>A </em>be a real, <u>symmetric </u><em>d </em>× <em>d </em>matrix. We say <em>A </em>is <em>positive semi-definite </em>(PSD) if, for all <strong>x </strong>∈ R<em><sup>d</sup></em>, <strong>x</strong><sup>&gt;</sup><em>A</em><strong>x </strong>≥ 0. We say <em>A </em>is <em>positive definite </em>(PD) if, for all <strong>x </strong>= 06, <strong>x</strong><sup>&gt;</sup><em>A</em><strong>x </strong><em>&gt; </em>0. We write 0 when <em>A </em>is PSD, and 0 when A is PD.

The <em>spectral theorem </em>says that every real symmetric matrix <em>A </em>can be expressed <em>A </em>= <em>U</em>Λ<em>U</em><sup>&gt;</sup>, where <em>U </em>is a <em>d </em>× <em>d </em>matrix such that <em>UU</em><sup>&gt; </sup>= <em>U</em><sup>&gt;</sup><em>U </em>= <em>I </em>(called an orthogonal matrix), and Λ = <em>diag</em>(<em>λ</em><sub>1</sub><em>,…,λ<sub>d</sub></em>). Multiplying on the right by <em>U </em>we see that <em>AU </em>= <em>U</em>Λ. If we let <em>u<sub>i </sub></em>denote the <em>i<sup>th </sup></em>column of <em>U</em>, we have <em>Au<sub>i </sub></em>= <em>λ<sub>i</sub>u<sub>i </sub></em>for each <em>i</em>. This expression reveals that the <em>λ<sub>i </sub></em>are eigenvalues of <em>A</em>, and the corresponding columns <em>u<sub>i </sub></em>are eigenvectors associated to <em>λ<sub>i</sub></em>.

<ul>

 <li><em>A </em>is PSD iff <em>λ<sub>i </sub></em>≥ 0 for each <em>i</em>.</li>

 <li><em>A </em>is PD iff <em>λ<sub>i </sub>&gt; </em>0 for each <em>i</em>. <strong>Hint: </strong>Use the following representation</li>

</ul>

<em>d</em>

<em>U</em>Λ<em>U</em><em>T </em>= X<em>λ</em><em>iu</em><em>iu</em><em>iT .</em>

<em>i</em>=1

<h1>5. Norms</h1>

<ul>

 <li>For <em>p </em>= 1<em>,</em>2<em>,</em>∞, verify that the functions k · k<em><sub>p </sub></em>are norms. Then, for a vector <em>x </em>∈ R<em><sup>n</sup></em>, show that</li>

</ul>

√

k<em>x</em>k<sub>∞ </sub>≤ k<em>x</em>k<sub>2 </sub>≤ k<em>x</em>k<sub>1 </sub>≤              <em>n</em>k<em>x</em>k<sub>2 </sub>≤ <em>n</em>k<em>x</em>k<sub>∞</sub>

and for each inequlaity, provide an example demonstrating that the inequality can be tight.

<ul>

 <li>For vectors <em>x</em>,<em>y </em>∈ R<em><sup>n</sup></em>, show that |<em>x<sup>T</sup>y</em>| ≤ k<em>x</em>||<sub>2</sub>k<em>y</em>k<sub>2 </sub>with equality if and only if <em>x </em>and <em>y </em>are linearly dependent. More generally, show that <em>x<sup>T</sup>y </em>≤ k<em>x</em>k<sub>1</sub>k<em>y</em>k<sub>∞</sub>. Note that this implies that; and that these are special cases of H¨older’s inequality.</li>

 <li>For <em>A </em>∈ R<em><sup>m</sup></em><sup>×<em>n</em></sup>, show that Trace(<em>A<sup>T</sup>A</em>) = <sup>P</sup><em><sub>ij </sub>A</em><sup>2</sup><em><sub>ij</sub></em>, and show that <sup>qP</sup><em><sub>ij </sub>A<sub>ij</sub></em><sup>2</sup> is a norm on <em>m</em>×<em>n </em> This is the Frobenius norm, denoted k·k<em><sub>F</sub></em>. Show that, in addition to satisfying the definining properties of a norm, the Frobenius norm is a submultiplicative norm, in that</li>

</ul>

k<em>AB</em>k<em><sub>F </sub></em>≤ k<em>A</em>k<em><sub>F</sub></em>k<em>B</em>k<em><sub>F</sub></em>

whenever the dimensions are such that the product <em>AB </em>is defined.

<ul>

 <li>Recall the definiton of the spectral norm of an <em>m</em>×<em>n </em>matrix <em>A </em>: k<em>A</em>k<sub>2 </sub>= <sup>p</sup><em>λ<sub>max</sub></em>(<em>A<sup>T</sup>A</em>) = <em>σ<sub>max</sub></em>(<em>A</em>), where <em>λ<sub>max</sub></em>(<em>A<sup>T</sup>A</em>) is the largest eigenvalue pf <em>A<sup>T</sup>A </em>and <em>σ<sub>max </sub></em>is the largest singular value of <em>A</em>. Show that the Frobenius norm and the spectral norm are unitarily invariant: if <em>U </em>and <em>V </em>are unitary (orthogonal in the real case) matrices, then k<em>U<sup>T</sup>AV </em>k<em><sub>ξ </sub></em>= k<em>A</em>k<em><sub>ξ</sub></em>, for <em>ξ </em>= 2<em>,F</em>.</li>

</ul>

<h1>6. Approximate Matrix Multiplication</h1>

Here, we will consider the empirical performance of random sampling and random projection algorithms for approximating the product of two matrices. You may use Matlab, or C, or R, or any other software package you prefer to do your implementations. Please be sure to describe what you used in sufficient detail that someone else could reproduce your results. Let <em>A </em>be an <em>n </em>× <em>d </em>matrix, with, and consider approximating the product <em>A<sup>T</sup>A</em>. First, generate the matrices A from one of three different classes of distributions introduced below.

<ul>

 <li>Generate a matrix <em>A </em>from multivariate normal <em>N</em>(1<em><sub>d</sub>,</em>Σ), where the (i, j)th element of Σ<em><sub>ij </sub></em>= 2 × 0<em>.</em>5<sup>|<em>i</em>−<em>j</em>|</sup>.(Refer to as GA data.)</li>

 <li>Generate a matrix <em>A </em>from multivariate t-distribution with 3 degree of freedom and covariance matrix Σ as before. (Refer to as T3 data.)</li>

 <li>Generate a matrix <em>A </em>from multivariate t-distribution with 1 degree of freedom and covariance matrix Σ as before. (Refer to as T1 data.)</li>

</ul>

To start, consider matrices of size <em>n</em>×<em>d </em>equal to 500×50. (So, you should have three matrices, one matrix <em>A </em>generated in each of the above ways.)

<ul>

 <li>For each matrix, approximate the product (<em>A<sup>T</sup>A</em>) with the random sampling algorithm we discussed in class, i.e., by sampling with respect to a probability distribution that depends on the norm squared of the rows of the input matrix. Plot the probability distribution. Does it look uniform or nonuniform? Plot the performance of the spectral and Frobenius norm error as a function of the number of samples.</li>

 <li>For each matrix, approximate the product (<em>A<sup>T</sup>A</em>) with the random sampling algorithm we discussed in class, except that the uniform distribution, rather than the norm-squared distribution, should be used to construct the random sample. Plot the performance of the spectral and Frobenius norm error as a function of the number of samples. For which matrices are the results similar and for which are they different than when the norm-squared distribution is used ?</li>

 <li>Now you will implement the matrix approximation technique on the MNIST dataset for handwritten digit classification. Details about MNIST dataset can be found at <a href="http://yann.lecun.com/exdb/mnist/">http://yann.lecun.com/exdb/mnist/</a><a href="http://yann.lecun.com/exdb/mnist/">.</a> We provide the dataset in <strong>.mat </strong>file so that you can easily import it into Matlab by using <strong>load(’mnist matrix.mat’)</strong>. To import the dataset in Python you can use:</li>

</ul>

<h1>import scipy.io data = scipy.io.loadmat(‘mnist matrix.mat’)</h1>

In <strong>.mat </strong>file you will find one matrix, <em>A </em>∈ R<sup>60000×784</sup>. For this matrix, approximate the product (<em>A<sup>T</sup>A</em>) with the random sampling algorithm we discussed in class, i.e., by sampling with respect to a probability distribution that depends on the norm squared of the rows of the input matrix. Plot the probability distribution. Dos it look uniform or nonuniform? Plot the performance of the spectral and Frobenius norm error as a function of the number of samples.

<a href="#_ftnref1" name="_ftn1">[1]</a> <em>I</em>[<em>X </em>∈C] := 1 if <em>X </em>∈C and 0 otherwise