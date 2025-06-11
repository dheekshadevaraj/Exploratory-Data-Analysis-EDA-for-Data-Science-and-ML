# **Exploratory Data Analysis (EDA) for data science and ML**

<center>
<img src="https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBMSkillsNetwork-GPXX0HE1EN/antonio_33943_A_fork_in_a_road_with_a_left_and_right_turn._A_ro_7a9c2af5-0772-49da-941a-4d2dbf54d10f.png" width="80%" alt="LDA illustration">
</center>

## __Table of Contents__

<ol>
    <li><a href="#Objectives">Objectives</a></li>
    <li>
        <a href="#Setup">Setup</a>
        <ol>
            <li><a href="#Install-required-libraries">Install required libraries</a></li>
            <li><a href="#Import-required-libraries">Import required libraries</a></li>
        </ol>
    </li>
    <li>
        <a href="#Regression">Regression</a>
        <ol>
            <li><a href="#Load-the-diabetes-data-set">Load the diabetes data set</a></li>
            <li><a href="#Add-some-missing-values">Add some missing values</a></li>
            <li>
                <a href="#Initial-data-preprocessing">Initial data preprocessing</a>
                <ol>
                    <li><a href="#One-hot-encoding">One-hot encoding</a></li>
                    <li><a href="#Make-a-train-test-split">Make a train-test split</a></li>
                </ol>
            </li>
            <li>
                <a href="#Perform-EDA">Perform EDA</a>
                <ol>
                    <li>
                        <a href="#A-look-at-the-beginning-and-end-of-the-data-set">A look at the beginning and end of the data set</a>
                    </li>
                    <li>
                        <a href="#Describe-the-DataFrame">Describe the DataFrame</a>
                    </li>
                    <li>
                        <a href="#Missing-values">Missing values</a>    
                    </li>
                    <li><a href="#Drop-missing-observations">Drop missing observations</a></li>
                    <li><a href="#Fill-in-missing-values-with-the-mean">Fill in missing values with the mean</a></li>
                    <li>
                        <a href="#Fill-in-missing-values-with-the-median">Fill in missing values with the median</a>
                    </li>
                    <li>
                        <a href="#Histograms-and-boxplots">Histograms and boxplots</a>  
                    </li>
                    <li><a href="#Correlation-matrix">Correlation matrix</a></li>
                    <li><a href="#Pair-plots">Pair plots</a></li>
                    <li><a href="#A-simple-function-to-perform-EDA">A simple function to perform EDA</a></li>
                </ol>
            </li>
        </ol>
    </li>
    <li>
        <a href="#Classification">Classification</a>
        <ol>
            <li><a href="#Import-the-iris-data-set">Import the iris data set</a></li>
            <li>
                <a href="#Perform-EDA-on-the-iris-data-set">Perform EDA on the iris data set</a>
            </li>
        </ol>
    </li>
</ol>

## Objectives

After completing this lab we are able to:

 - Perform EDA using a set of very simple and easy-to-memorize Python commands
 - Interpret key EDA plots and statistics
 - Improve a prediction model by using information obtained through EDA
 - Perform basic feature engineering
 - Detect and handle outliers
 - Deal with missing data
   
## Setup
For this lab, we use the following libraries:

*   [`pandas`](https://pandas.pydata.org/?utm_medium=Exinfluencer&utm_source=Exinfluencer&utm_content=000026UJ&utm_term=10006555&utm_id=NA-SkillsNetwork-Channel-SkillsNetworkCoursesIBMML0187ENSkillsNetwork31430127-2021-01-01) for managing the data
*   [`NumPy`](https://numpy.org/?utm_medium=Exinfluencer&utm_source=Exinfluencer&utm_content=000026UJ&utm_term=10006555&utm_id=NA-SkillsNetwork-Channel-SkillsNetworkCoursesIBMML0187ENSkillsNetwork31430127-2021-01-01) for mathematical operations
*   [`SciPy`](https://scipy.org/) for additional mathematical operations beyond those provided by `numpy`
*   [`sklearn`](https://scikit-learn.org/stable/?utm_medium=Exinfluencer&utm_source=Exinfluencer&utm_content=000026UJ&utm_term=10006555&utm_id=NA-SkillsNetwork-Channel-SkillsNetworkCoursesIBMML0187ENSkillsNetwork31430127-2021-01-01) for machine learning and machine learning pipeline-related functions
*   [`seaborn`](https://seaborn.pydata.org/?utm_medium=Exinfluencer&utm_source=Exinfluencer&utm_content=000026UJ&utm_term=10006555&utm_id=NA-SkillsNetwork-Channel-SkillsNetworkCoursesIBMML0187ENSkillsNetwork31430127-2021-01-01) for visualizing the data
*   [`Matplotlib`](https://matplotlib.org/?utm_medium=Exinfluencer&utm_source=Exinfluencer&utm_content=000026UJ&utm_term=10006555&utm_id=NA-SkillsNetwork-Channel-SkillsNetworkCoursesIBMML0187ENSkillsNetwork31430127-2021-01-01) for additional plotting tools
*   [`MissingNo`](https://github.com/ResidentMario/missingno) for missing data analysis and visualizations
*   [`fasteda`](https://github.com/Matt-OP/fasteda) for fast and easy EDA
