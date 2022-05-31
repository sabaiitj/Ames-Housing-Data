| Score |     |
|---|---|
| **0** | *Project fails to meet the minimum requirements for this item.* |
| **1** | *Project meets the minimum requirements for this item, but falls significantly short of portfolio-ready expectations.* |
| **2** | *Project exceeds the minimum requirements for this item, but falls short of portfolio-ready expectations.* |
| **3** | *Project meets or exceeds portfolio-ready expectations; demonstrates a thorough understanding of every outlined consideration.* |

Section	|	Score	|	Notes
------	|	------	|	--------
**Problem Statement**	|	**2**	|
Is it clear what the student plans to do? 	|	3	|	Extremely.
What type of model will be developed? 	|	3	|	Linear regression, Ridge, Lasso.
How will success be evaluated? 	|	1	|	Unstated in problem statement, R2 score.
Is the scope of the project appropriate? 	|	1	|	It is the minimum required of the student.
Is it clear who cares about this or why this is important to investigate?	|	2	|	Yes. Home buyers and sellers and their needs.
 Does the student consider the audience and the primary and secondary stakeholders?	|	2	|	Yes.
**Data Cleaning and EDA**	|	**2**	|
Are missing values imputed appropriately? 	|	3	|	Yes, algoirthmically for each category.
Are distributions examined and described? 	|	2.5	|	Yes, could use more description.
Are outliers identified and addressed? 	|	3	|	Yes.
Are appropriate summary statistics provided? 	|	1	|	Full correlation analysis, no mean/std.
Are steps taken during data cleaning and EDA framed appropriately? 	|	2	|	Mostly. There are sections of many charts with no indication as to what should be gleaned from them.
Does the student address whether or not they are likely to be able to answer their problem statement with the provided data given what they've discovered during EDA?	|	1	|	Some noting of linear relationships to target.
**Preprocessing and Modeling**	|	**3**	|
Are categorical variables one-hot encoded? 	|	3	|	Yes.
Does the student investigate or manufacture features with linear relationships to the target? 	|	3	|	Yes.
Have the data been scaled appropriately? 	|	3	|	Yes.
Does the student properly split and/or sample the data for validation/training purposes? 	|	3	|	Yes.
Does the student utilize feature selection to remove noisy or multi-collinear features? 	|	3	|	Yes.
Does the student test and evaluate a variety of models to identify a production algorithm (AT MINIMUM: linear regression, lasso, and ridge)? 	|	3	|	Yes.
Does the student defend their choice of production model relevant to the data at hand and the problem? 	|	2	|	Not quite to the problem, but to problems experienced while modeling.
Does the student explain how the model works and evaluate its performance successes/downfalls?	|	0	|	No.
**Evaluation and Conceptual Understanding**	|	**2**	|
Does the student accurately identify and explain the baseline score? 	|	1	|	No, but that is not really a thing with R2.
Does the student select and use metrics relevant to the problem objective?	|	3	|	Yes.
Is more than one metric utilized in order to better assess performance? 	|	0	|	No.
Does the student interpret the results of their model for purposes of inference? 	|	0	|	No.
Is domain knowledge demonstrated when interpreting results? 	|	2	|	Implicit understanding show by handling and noting of overfitting issues.
Does the student provide appropriate interpretation with regards to descriptive and inferential statistics?	|	3	|	Yes.
**Conclusion and Recommendations**	|	**1**	|
Does the student provide appropriate context to connect individual steps back to the overall project?	|	3	|	Yes.
 Is it clear how the final recommendations were reached? 	|	2	|	Yes.
Are the conclusions/recommendations clearly stated? 	|	2	|	Yes.
Does the conclusion answer the original problem statement? 	|	1	|	Yes. Problem statement was a bit vague but you did create a model to predict house prices.
Does the student address how findings of this research can be applied for the benefit of stakeholders? 	|	0	|	Your conclusions focused mainly on the limitations of your data. While it is important to be aware of and transparent with the limitations of your models you should also try to include a section on how your model could be useful despite those limitations.
Are future steps to move the project forward identified?	|	1	|	Try to be specific about what the next steps you would like to take with the project are.
**Project Organization**	|	**2**	|
Are modules imported correctly (using appropriate aliases)? 	|	3	|	Yes.
Are data imported/saved using relative paths? 	|	3	|	Yes.
Does the README provide a good executive summary of the project? 	|	1	|	Yes, minus the conclusion.
Is markdown formatting used appropriately to structure notebooks? 	|	3	|	Yes.
Are there an appropriate amount of comments to support the code? 	|	3	|	Yes.
Are files & directories organized correctly? 	|	0.5	|	Organization scheme is not understood by me. Old code appears to be in the "untitled" folder and main folder contains several conceptually different types of files.
Are there unnecessary files included? 	|	0	|	Yes, original.md, suggestions.md, and potentially old/broken notebooks.
Do files and directories have well-structured, appropriate, consistent names?	|	1	|	Consistent, yes, but lacking structure. Folders should be named by what they contain, and notebooks should be named by their functional purpose.
**Visualizations**	|	**3**	|
Are sufficient visualizations provided? 	|	3	|	Yes.
Do plots accurately demonstrate valid relationships? 	|	3	|	Yes.
Are plots labeled properly? 	|	2.75	|	Mostly, minus some title-less histograms.
Are plots interpreted appropriately? 	|	3	|	Yes.
Are plots formatted and scaled appropriately for inclusion in a notebook-based technical report?	|	3	|	Yes.
**Python Syntax and Control Flow**	|	**3**	|
Is care taken to write human readable code?	|	3	|	Yes.
Is the code syntactically correct (no runtime errors)? 	|	3	|	Yes.
Does the code generate desired results (logically correct)?	|	1	|	The output of your models appears to always be 0 or infinity. Perhaps something went wrong with scaling the target?
 Does the code follows general best practices and style guidelines? 	|	3	|	Yes.
Are Pandas functions used appropriately? 	|	3	|	Yes.
Are sklearn methods used appropriately?	|	3	|	Yes.
