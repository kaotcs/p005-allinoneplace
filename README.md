# All in One Place

Create a loyalty program to the high-value customers by clusternig.

<img src="https://github.com/kaotcs/p005-allinoneplace/blob/main/img/785054-ecommerce-istock-020119.jpg" alt="All in one place"
	title="AIOP"  width="100%" height="500" />

## 01 BUSINESS PROBLEM
A UK-based online retail store has captured the sales data for different products for the period of one year (Nov 2016 to Dec 2017). The organization sells gifts primarily on the online platform. The customers who make a purchase consume directly for themselves. There are small businesses that buy in bulk and sell to other customers through the retail outlet channel.

Find significant customers for the business who make high purchases of their favourite products. The organization wants to roll out a loyalty program to the high-value customers after identification of segments.

## 02 BUSINESS ASSUMPTIONS
<ul>
<li>The customer must have at least more than one purchase during the period analyzed.</li>
<li>The customer revenue considered do not take account the return the product. It was eliminated by equalizing with previous purchase. </li>
</ul>

## 03 SOLUTION STRATEGY
The strategy adopted was the following:

<b>Step 01.</b> Data Description: Searching for missing values, checking data types and preliminary statistical description.

<b>Step 02.</b> Feature Engineering: Creating new features to improve the features for clustering.

<b>Step 03.</b> Data Filtering: Data with no information or containing inputs which does not match to the scope of the project were removed.

<b>Step 04.</b> Exploratory Data Analysis: Analyzed the features created by verifiy if is possible to make a cleaner dataframe for clustering. New features were created and other removed or improved. At the end, it was also made a space study with PCA, t-SNE, UMAP and tree-based embedding.

<b>Step 05.</b> Data Preparation: Transforming the data for inputing to machine learning model. Most of jobs were rescaling and transforming the features values.

<b>Step 06.</b> Feature selection: Not Applied.

<b>Step 07.</b> Machine learning modelling: Identifying the best k for the cluster. It was used k-Means, GMM and Hierarchical Clustering and the metric employed to choose the best k was silhouette score.

<b>Step 08.</b> Hyperparameter Fine Tunning: It was employed K-means with k=5, since the embedded space did not have a overlap between clusters (k-Means and GMM had the same score for silhouette).

<b>Step 09.</b> Cluster Analysis: With 5 clusters created, it was chosen with the best average revenue. The insiders cluster have the double revenue compared to second place and it is represented by 117 customers.

<b>Step 10.</b> Exploratory Data Analysis for "Cluster Insiders": It was developed and hypothesis mindmap and the business problem question was answered in this step.

## 04 TOP 3 DATA INSIGHTS

* 82% of database is represeted by new customers or just made one order since the registration.

* Most of customers are from UK and Europe (up to 90%), but there are other from other countries.

* 117 customers indicated in the insiders cluster represent 7% of annual revenue.

## 05 MACHINE LEARNING MODEL APPLIED

The following machine learning algorithms were used to predict sales:

* k-Means;
* Gaussian Mixture Models (GMM);
* Hierarchical Clustering;

## 06 MACHINE LEARNING MODEL PERFORMANCE

The silhouette score for each model is indicated bellow:

<img src="https://github.com/kaotcs/p005-allinoneplace/blob/main/img/silhouette.jpg" alt="ML peformance"
	title="AIOP"/>

## 07 DEPLOYMENT
It was used AWS plataform (S3, RDS and EC2) to deploy the result of this clustering. The insiders clusters data can be visualized at Metabase platform. (Link will be available soon)

## 08 CONCLUSION
This insiders clusters represet a great path to marketing team and strategical aprouch to BI team improvement of revenue and keep the sales higher. The other customers which is not included should be analyzed and it is importante to create some trigger to pull them to insiders clusters.

## 08 LESSONS LEARNED / NEXT STEPS AND IMPROVEMENTS
Clustering problems is an unsupervised problem which does not have the right answer. It was made 9 cicles where it was made a deeper look in each feature. At this point, it was selected the best result that should be improved exploring new features or creating new ones from existing data.
