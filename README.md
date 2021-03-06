# credit-risk-modeling-with-python

The likelihood that a borrower would not repay their loan to the lender is called __credit risk. Collection cost__ is the cost of recovering the money the borrower was not able to pay. Risk based pricing considers either increasing the interest rate of lending or asking for higher collaterals. Hence, it is important to estimate credit risk of a borrower. One main reason for economic crisis is to lend money to ineligible borrowers or ones with lower credit scores or higher credit risk.
 
Losses in a loan can be either due to borrower specific factors, economic environment or the combination of two. Here we will build models to estimate espected loss (expected credit loss)

<h2><a id="ecl">1. Expected Credit Loss</a></h2>

The amount a lender might lose by lending to a borrower. The expected Loss is calculated as product of 

<ol>
<li><b>Probability of Default (PD)</b>: is the likelihood that the borrowers won't pay their debt in full or on time. </li>
<li><b>Loss Given Default (LGD)</b>: is share of an asset that is lost if a borrower defaults. It is proportion of the total exposure that cannot be recovered by the lender once a default has occured.</li>
<li><a>Exposure at Default (EAD)</b>: is total value that a lender is exposed to when a borrower defaults. It is maximum a bank can lose when a borrower defaults on the loan.</li>
</ol>

<h2><a id="regulations">2. Capital Adequacy, Regulations and the Basel II Accord</a></h2>
<p>Banks must conduct their business without risking the stability of the economic system. Regulators rules: </p>
<ol>
<li>Regulate bank operations and hence <u>reduce risky behavior</u>.</li>
<li>Gurantee to the public that the <u>banking system is in good health</u>.</li>
</ol>

<p>Banks must hold sufficient capital to absorb losses from defaulting loans. This obligation is called <b>Capital Requirement (Capital adequacy or regulator capital). The Capital requirement postulates that the bank must hold capital which is a certain percent of the risk weighted assets loans. The ratio is called Capital Adequeacy ratio. <b>Basel II Accord</b> defines: </p>
<ul>
<li>How much capital banks need to have</li>
<li>How capital is defined</li>
<li>How capital is compared against risk-weighted assets</li>
</ul>

<p>Basel II Accord defines <b>Minimum Capital Requirements</b> based on: </p>
<ol>
<li>Credit Risk<ol>
<li>Standardized Approach (SA): Capital to be held should be a % of the total exposure. This is not very flexible and banks end up holding lot more capital than required.</li>
<li>Internal Ratings Based (IRB) Approaches: Allows banks to establish their own credit ratings, have precise calculations about the held exposure capital for each individual exposure and allocate resources to cover losses. This in turn allows them to be more profitable.<ul>
<li>Foundation Internal Ratings Based (F-IRB) Approach</li>
<li>Advanced Internal Ratings Based (A-IRB) Approach</li>
</ul></li>
</ol></li>
<li>Operational Risk</li>
<li>Market Risk</li>
</ol>

<h3>What can be estimated internally vs sourced from externa parties under different Credit Risk measuring approaches</h3>

<img src="./Images/BaselI Accord allowed modeling.png" />

<h3>Capital held for Countries under Standardized Approach</h3>

<img src="./Images/SA-Capital-countries.png" />

<h3>Capital held for Companies under Standardized Approach</h3>

<img src="./Images/SA-Capital-companies.png" />

<h2><a id="modeltypes">3. Models for different components to measure Credit Risk</a></h2>

<img src="./Images/modeltypes_for_differentcompoents.png" />

Application model: Used in first stage - to make a decision on first application to extend loan. 

Behavioral Model: After loan is granted. Can also be used to check if additional loan should be granted.


<h2><a id="dependentvar">4. Dependent Variables</a></h2>

<ol>
<li>PD Model: Logistic Regression (Loan Status variable)</li>
<li>LGD Model: Beta Regression (Recoveries)</li>
<li>EAD Model: Beta Regression(Total recovered principle column)</li>
</ol>


<h2><a id="featureprocessing">5. Feature Processing</a></h2>
