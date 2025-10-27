# DA5401
DA5401 Data Analytics Lab -- Assignments and Solutions

## Course Objectives
* Learn to transform a business problem into a data science problem
* Learn to use Machine Learning to solve data-driven decision making.
* Evaluating the results of Machine Learning modeling.
* Visualization and interpretation of the experimental results.
* Statistical analysis and model selection.

## Prerequisites
* DA5400 or any other equivalent courses on Machine Learning and/or Pattern Recognition
* Fluency in Python programming
* Ability to use third-party libraries such as Sklearn, NumPy, Pandas
* Linux or Mac or Windows WSL environment (Windows native discouraged)

## The Process
* We will meet every week on Monday (P-slot)
* At least one hour of lecture will be given every week to introduce you to the practical aspects of an ML/Analytics topic.
* Students are expected to use the remaining time in the slot to do their assignments or clarify their queries.
* There will be at least **eight** assignments spread across the semester.
* At least **three** assignments will be evaluated in the class within the same evening.
* The remaining take-home assignments will be given **~10 days** for submission.
* The end-semester exam will be a Data Challenge competition.
* 75% weightage to the assignments, 20% to the data challenge (rank + report + viva) and 5% to class interaction.

## References
* Sarah Guido, Andreas Muller., [Introduction to Machine Learning through Python](https://duchesnay.github.io/pystatsml/), 2024
* Gareth James et al., [Introduction to Statistical Learning](https://www.statlearning.com/), 2024

## End-Semester Competition
[DA5401 Data Challenge 2025](https://www.kaggle.com/competitions/da5401-2025-data-challenge/)

### Overview

Metric learning is a type of machine learning that focuses on learning a distance function to measure how similar or different objects are from each other.

The quality of conversational AI agents hinges on practical, automated evaluation. In this competition, participants are tasked with building a metric learning model to predict the "fitness" or similarity score between a specific AI Evaluation Metric Definition and a corresponding Prompt-Response Text Pair.

The ability to accurately model this fitness is crucial for automatically generating and curating high-quality test datasets, ensuring that the test cases are genuinely aligned with the evaluation goals, and ultimately, building better, more reliable AI agents.

*Goal*: Given a metric definition (text embedding) and a prompt-response pair (text), predict the relevance or fitness on a scale of 1-10.

### Description

We have an AI Evaluation system that tests a target conversational AI agent with a variety of test prompts encompassing use cases from different business domains. The evaluation process fires up the test prompts for each evaluation metric to the AI agent, followed by assessing the correctness or fitness of the response received against the definition of the evaluation metrics. The assessment score estimated by the evaluation system is in the 0-1 range.

For each evaluation metric (refer to metric_names.json), we have manually curated test prompts and expected responses to check if the agent's response matches them. We have definitions (text, not shared) of evaluation metrics, and the test (prompt, response) pairs are created to align with the objective of the evaluation metrics. We test the fitness of a curated (prompt, response) pair against the metric definition by passing the texts to an LLM judge. The judge rates the fitness in the 0-10 range. This process creates a dataset of a) metric definition string and b) prompt-response text pair.

Participants will receive a dataset consisting of three key components: Metric Definitions (text embeddings), Prompt-Response Pairs (JSON), and the target fitness scores (between 0 and 10), which represent the ground-truth fitness as assessed by a sophisticated LLM judge. Your task is to train a model that takes the Metric Definition (embedding) and the Prompt-Response Pair (text) as input and predicts the Target Fitness Score (0-10). This is essentially a regression (or classification?) problem framed within a metric learning context, where the model must learn the semantic distance (or similarity) between two pieces of text that describe the intent (the Metric) and the test case (the Pair).

### Evaluation

The objective is to predict the score as close to the actual score of the test data. Note that the scores of the training data are discretized into whole numbers in the range 0-10. The testing data's ground truth is also discretized, allowing you to hack the solution further.  We use RMSE to evaluate your predictions against the ground truth. The lower the RMSE value, the better your prediction performance.

### Rules
There are three parts to this competition. The first part is your position on the leaderboard based on your reported classification performance. The second part is an online test (will be conducted separately for 30 minutes) to validate your understanding of the problem and solution(s). The third part is your report that captures all the details of your experiments and your final solution to the challenge.

The leaderboard scores will be divided into six groups, each with a definite range of performance scores. The ranges shall be published by the end of the competition so that you will know which bin you fall into. The total points allocated for the leaderboard position are 60. The top bin will get the full 60 points, and the remaining bins will receive 55, 50, 45, 40, and 30, respectively, out of 60. The point allocation for the online test and the report evaluation is 20 points each.

The online test will serve as an equivalent of the F2F viva. So, expect questions that might be asked in the viva to appear in the online test. The test URL shall be published around the end of the competition.

Your report should elucidate your technique(s) and method(s) to solve the problem. The report should contain details about your initiatives on the following items:

Data Engineering Sampling EDA with visualization Model Selection with performance metrics Hacks and Workarounds that you have invented Training and Validation performance tables of your final model.

All said and done, Integrity is our character, and Transparency is our strength! Only Solo teams are welcome Apply yourself! Have fun!

## Archive
* 2024: [Data Challenge competition](https://www.kaggle.com/competitions/da5401-2024-ml-challenge)
