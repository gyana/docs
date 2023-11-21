# Automate

How to keep your dashboards up to date.

Automate is a single interface to view, run and schedule everything in your project.

**Think of it like your mission control**. You'll get a top of level view of how everything fits together, and the tools to keep it running reliably and up to date.

## 👀 Reviewing your work

To start with, you can view all your integrations, workflows and dashboards as connected **steps** on a single canvas.

💡 Note that unlike workflows, the positions and relationships are generated automatically. You can drag-n-drop the items on the canvas, but it will only be temporary.

The relationships track the flow of data through your project - for example, a workflow is linked to an integration, if it uses that integration in a **Get data** node. If you've accidentally referenced the wrong data source in a dashboard or workflow, it should be easy to spot here.

Your integrations and workflows have a **status indicator** in top right, with information on the most recent run. The possible values are **⏱ Pending, ▶️ Running, ✅** **Success** and **❌** **Failed**.

If a step has **❌** **Failed**, you can click the **Edit** button to navigate to that integration or workflow, understand what went wrong, fix it, and re-run it.

💡 Remember that until you fix a failed step, anything that depends on that step will not get the latest version of the input data.

## ▶️ Running your project

Click the **Run All** button in the top right to run all your integrations and workflows.

They are run in dependency order - for example, if a workflow depends on an integration, we run that integration first so the workflow gets the latest data.

As the project runs, you'll see the status indicator for each step update from **⏱ Pending**, to ▶️ **Running** and finally ✅ **Success** or **❌** **Failed**. When all steps are completed, you'll get an alert.

We keep track of all the **historical runs**, which you can view in **Settings & History**. The project run is a success, if all the individual steps ran successfully, otherwise it is failed.

💡 Currently, connectors are ignored in Run All. In future, we do plan to add this as an option.

## 📅 Setting up a daily schedule

If you're happy that your steps are running successfully, it's time to schedule them to run automatically. You can do this on the settings pages for individual integrations and workflows.

On the Automate page, scheduled steps appear with a light green background, so it is easier to track what is and isn't scheduled.

💡 Note that you cannot schedule uploads, and connectors are always scheduled (but we plan to add an explicit option in future).

By default, they will run at **00:00 GMT**. You can configure the daily sync time (as an hour) in the Automate page under **Settings & History**, and the timezone in the **team settings**. For example, you can run your project at 6am in Pacific Time.

As with **Run All**, your integrations and workflows will run in dependency order, and you view the status of current and historical runs.