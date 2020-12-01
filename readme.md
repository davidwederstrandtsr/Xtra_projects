# Kaggle's Kickstarter Data Project

- https://www.kaggle.com/kemical/kickstarter-projects
## Goal: Predict whether or not a project will be successful

### Planning
  - Make a plan for what your time on the project will look like
  - Write down the steps that need to happen in each pipeline phase
  - The goal of planning is to have a guiding framework so that you don't go
    too "off the rails" in any one of the pipeline phases, and so that you
    aren't wondering what to do next or uncertain about how to spend your time

### Acquire
  - Download the csv file from kaggle, don't worry about automating this
  - import the csv as a dataframe
  - view the statistical information of the dataframe
      - .describe(), .info(), .shape
      - look for nulls .isna()
      - idetify the columns and the purpose of their values

- Column and purpose
    - ID: identification number assigned by Kickstarter
    - name: Business name
    - category: Product type  e.g. Poetry
    - main_category: Parent category  e.g. Publishing
    - currency: Country currency is listed as.  e.g. USD for United States Dollar
    - deadline: Date pledged goal needs to be reached
        - 100% of the goal must be reached by this date or no funds are collected
    - goal: Monetary amount required for a successful Kiskstart
    - launched: Date the kickstart is launched
    - pledged: Total monetary amount pledged from around the world
    - state: Kickstarts that have either succeed or failed
    - backers: Number of pledgers
    - country: Origin of company requesting funding
    - usd_pledged: Pledged in USD, converted by Kickstarter
    - usd_pledged_real: Pledged in USD, converted by Foreign exchange rates and currency conversion JSON API
    - usd_goal_real: Goal in USD, converted by Foreign exchange rates and currency conversion JSON API

### Preperation
  - narrow scope to just projects that have either succeeded or failed
  - choose a subset of the columns to focus on
  - do a train-test split
  - don't spend a lot of time here, for example, don't worry about building an
    automated solution for prep, just having the code in a notebook you can
    re-run is fine

### Explore
  - Be very deliberate in your planning here
  - Write down any questions or hypothesis that you have about the data
  - Refine and narrow the initial list of questions into 3 - 7 specific,
    answerable questions
  - For each questions, write down several bullet points of visualizations you
    can make to answer the question
  - Once all of the above is done, write the python code to produce the
    visualizations

### Modeling
  - Establish a baseline model that predicts the most common class from the
    target, measure the baseline model's accuracy
  - Fit several models and measure their performance
      - LogisticRegression
      - KNN
      - Decision Tree
  - Run the best model on your test data to get an idea of out-of-sample error
