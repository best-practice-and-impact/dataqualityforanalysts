# Data Quality for Analysts
## Introduction
Good quality data is data that is fit for purpose. 
This means that the data you are working with suits your needs. When analysing a dataset, you will be making decisions about what values you want to include or any cleaning you need to do. These decisions may be based on your knowledge of the analysis you would like to conduct, assumptions about the data or conversations you have had with the collector/supplier about it, and your experience with the type of data you are working with. During this process you are assessing how fit for your purpose – your analysis - the data is and what you need to do to mitigate any problems you have found. All these decisions are critical to the success of your analysis, and in ensuring as high a quality output as you can obtain based on the data you received. There is no problem   with having an analytical output where the quality has been prohibited by the data you have been using; no data is perfect. 
What is important is that you the analyst:
-	Understand how well the data fits the purposes you are using it for
-	Can articulate the effects of any strengths and limitations of the data on your analysis
-	Can communicate the above with the users of your outputs

Analytical outputs in government are often used to make big decisions which effect all members of society. It is therefore critical that we know how to assess and communicate quality across this ecosystem, from collection to analysis to decision making. This will support you the analyst in your work, as well as the policy makers and data collectors whose roles are influenced by the analysis you produce. Delivering not just the analysis, but the information you used to get there and the potential strengths and limitations of it, allows for essential context to be included in the decisions which are made with it. 

There are further benefits for you the analyst in conducting this work. Increasing communication about quality across this ecosystem increases the likelihood that quality issues are flagged, understood, and addressed where possible. Analysts may often feel that they “bear the brunt of poor-quality data”, developing complex work arounds to make the data fit their needs and disproportionately burdened by cleaning the data. Having the tools to understand what these quality issues are and communicate them both to data collectors and policy makers makes it much easier to solve these problems at source.  

This may feel like extra work in the short term, but there are so many work arounds that you are probably engaging with on a regular basis which could be avoided if there was a greater openness to communication about quality. These may look like:
- Cleaning, so much cleaning (this may also be referred to as data cleansing* reference see the footnote *)    
- Lots of back and forth with data collectors/suppliers to understand the provenance of data (what does column x mean?)
- *** Add to

You will have no doubt developed your own ways of assessing, mitigating and communicating quality, perhaps ad hoc over time or using examples of best practice you have found elsewhere. This guidance will streamline this process for you by compiling best practice, providing you with a one stop shop for how to assess and communicate quality as government analysts. That being said, knowing how much experience there exists across government, we are seeking to develop this guidance both for and with you. This is why we are hosting it on GitHub, to give you chance to input your ideas and experiences. Instructions for how to do this EXIST WHERE?  

## How to understand and measure data quality: the DQ dimensions
The definition of data quality as fitness for purpose might sound difficult to understand and assess in practice. This is why the DQ dimensions are a good way to describe your data and assess their quality level. A DQ dimension is ‘a recognised term […] to describe a feature of the data that can be measured […] to determine the quality of data’ ([DAMA White paper](https://www.dama-uk.org/resources/Documents/DAMA%20UK%20DQ%20Dimensions%20White%20Paper2020.pdf)).

There is no one set of dimensions on which all data quality practitioners agree on. In 2013, DAMA UK published best practice advice on this and suggested six main dimensions. Here we provide only a brief working-level definition. A more in-depth description and examples for each dimensions can be found in the [government data quality framework](https://www.gov.uk/government/publications/the-government-data-quality-framework/the-government-data-quality-framework) and [DAMA White paper](https://www.dama-uk.org/resources/Documents/DAMA%20UK%20DQ%20Dimensions%20White%20Paper2020.pdf).
1.	Completeness: a measure of the presence of non-blank values (or absence of blank/null/empty) values;
2.	Uniqueness: a measure of whether the data contains only one record for each entity represented;
3.	Timeliness: a measure of whether the data accurately reflects the period intended and it up-to-date;
4.	Validity: a measure of whether the data conforms to the format, range, and syntax as expected;
5.	Accuracy: a measure of whether the data matches reality and correctly describes the real world or object intended;
6.	Consistency: a measure of whether the data do not contradict other values describing the same entity. 

The relative importance of the dimensions will need to be judged and decided on by the data analyst, based on the purpose of the data and its analysis. For instance, when dealing with time-sensitive reports, you might want to give more importance to timeliness over completeness in your assessment. This does not imply that it is not important to have complete data, but rather that for your specific purpose, is better to have more frequently updated data, then having a very high completeness rate. This is also why it is good practice to review your assessment at specific points in time, as circumstances and priorities might change, affecting the quality assessment.

It is also important to note that quality does not equate to data scoring 100% against all dimensions. No real-life dataset will be ‘perfect’, and that should not be our aim. Rather, you should consider whether the assessment obtained is enough to give confidence in your results, and what implications this might have on the robustness and credibility of results based on that data. For all these reasons, it is important that you document all the steps undertaken for the assessment, from defining what your purpose is, to considerations of the impact of quality on your results. This will help ensure that your analysis can be quality assured and reproduced by others. 

A final, important consideration on the dimensions: even if data is satisfactory under all the dimensions, the data could still not be fit for purpose. You should consider further aspects, like relevance, usability, confidence in the data, value, etc. For instance, an organisation might need data for a decision, but this data is not collected.

## How to assess the quality of your data
We have now found out what data quality is, and what the dimensions are. We now look into how to assess how the data scores against each dimension.
Before proceeding, an important clarification. Your organisation might have data quality or data management experts who might have performed checks on quality already. Or you might be using data from a data supplier or provider that has quality checks in place. If this is the case, they should be able to provide you with details on these assessments already, or you might want to have a conversation with them on what has been done before. Remember that their definition of fit for purpose might be different than yours, so you might still need to proceed with your assessment (or agree with them on how to include your purposes in the picture for their assessments). However, establishing a strong relationship with your data providers or data colleagues is always beneficial. Your data colleagues will be able to identify and mitigate the causes of low quality, applying tools such as root cause analysis that are outside the scope of this guidance (reference to DAMA book here).

For the purposes of this guidance, the starting point is a technically correct data file that can be imported into R or Python. We consider a data file as technically correct if the dataset that has suitable variables (columns) names and is stored as the appropriate data object (data.frame in R and xx in Python). (reference to importing data here in the right format and changing variable names).

### Step 1: descriptive and summary statistics 
For the first stage of your assessment, you will need the data for your analysis at hand. Q: what do we want to suggest for when merging of different datasets is required? @LuciaBarbone thinking is that we should suggest to do a merging and keeping all, independently from the number of matches. You should then conduct a number of checks, descriptive statistics, and summaries that will help you understand how your data is scoring against each dimension. The following table suggests what checks are appropriate for each dimensions, as well as useful R commands. However, you are always welcome to add more or use different ones if more appropriate for your data!

### How to mitigate against less than ideal data quality

## Useful links and resources
### Data Quality
- [Government Data Quality Framework](https://www.gov.uk/government/publications/the-government-data-quality-framework/the-government-data-quality-framework)
- [DAMA White paper](https://www.dama-uk.org/resources/Documents/DAMA%20UK%20DQ%20Dimensions%20White%20Paper2020.pdf)

### Data Cleaning
- [Introduction to data cleaning with R](https://cran.r-project.org/doc/contrib/de_Jonge+van_der_Loo-Introduction_to_data_cleaning_with_R.pdf)

