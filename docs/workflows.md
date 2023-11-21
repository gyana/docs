# Workflows

How to work with data and build new sources in Gyana.

A workflow is a visual editor to clean, transform, and analyse your data.

**Think of workflows like spreadsheets, but better suited for data analytics.** Instead of manually deleting rows or adding formulas, you define each transformation once and they'll be run automatically in future.

Workflows are the nuts and bolts of your data analytics work. Use them to prepare data, build segments and calculate new metrics.

## 🏗 Building your workflow

To build a workflow, you drag-n-drop nodes onto the canvas and connect them together. Data flows from the **right side** (output) of a node into the **left side** (input) of the next node. Certain nodes (e.g. joins) have multiple inputs.

There are two special nodes:

*   **Get data** will import data from an integration or another workflow
    
*   **Save data** will export data and make it available in other workflows or dashboards
    

💡 You should always start with a **Get data** node, otherwise you'll have no data to work with!

To configure a node, click the edit button below it (or double click it). You edit the configuration, and preview the results before saving. We've written a guide for every node if you run into any issues.

💡 For example, in the filter node, you'll need to choose the column ("city"), predicate ("equals") and value ("London").

At the moment, we have nodes for most common data transformations, including a formula editor (think Excel). If you see something obvious missing, do let us know!

## ▶️ Running your workflow

While you build your workflow, any preview is just temporary. To save the results, you need to click **Run** and wait for it to complete successfully.

💡 Running a workflow is optional. You only need to do it if you plan to use the results in another workflow or dashboard.

If the workflow fails, you'll see an error indicator on the relevant node. Once you've opened the node and fixed the issue, you'll be able to run the workflow again.

After you've run a workflow for the first time, data from the **Save data** nodes will be available in other workflows and dashboards. You are free to modify and run a workflow as often as you like, and the changes will be reflected in downstream workflows and dashboards automatically.

💡 By default, workflows only run when you click **Run workflow**. To learn about scheduling workflows, take a look at our Automate feature.

## 🙌 Collaborating on workflows

If you're working in a team, it's important that your team members can understand and modify your workflows without introducing mistakes.

We've added a few features to make this easier:

*   You can **rename** individual nodes to describe what they do
    
*   Use **format** to turn your spaghetti mess into a clear layout
    
*   Add **text nodes** to explain what's happening
    

## 🔮 What does the future hold?

Workflows are a visual way to write SQL. If you hadn't realised that yet - great, we are doing our job! We believe you shouldn't need to learn SQL to do data analytics. Our focus is to continue to make improvements everywhere to keep things that way.

Alongside that, we're planning to add special nodes for features like language analysis, text generation, geo-location, marketing enrichments and third party APIs. We've already built a sentiment analysis node in this direction. Watch this space!