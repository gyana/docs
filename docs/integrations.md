# Integrations

How to connect your data sources to Gyana.

<div style="position: relative; padding-bottom: 56.25%; height: 0;"><iframe src="https://www.loom.com/embed/6276920be4e344afa68c0a3386fa5669?sid=58defafb-81c8-45ab-9761-cf8f849479fe" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe></div>

An integration is a source of data, like a CSV file, Google Sheet, ads account, database, or web app.

Since you can't do data analytics without data (!), it's our top priority to make it as effortless as possible for you to integrate data from anywhere.

💡 If you're having difficulties importing data, take a look at our troubleshooting guide.

## 🚛 Choosing your import method

Gyana has a wide variety of ways to connect to your data. At a high level, we recommend three possible approaches:

*   Dedicated **connectors** with one-click setup, for sources like Google Analytics
    
*   More flexible options to build your own connections with **Google Sheets**, **CSV upload**, **custom APIs** and **webhooks**
    
*   **Custom integrations** built by the Gyana team for your project
    

We'll go through them one by one.

## Connectors

Connectors are specially made integrations for specific data sources, like Google Analytics or Facebook Ads. We support 80+ connectors out of the box, with more coming every month.

Connectors are the best choice, if available. After a one-time authorization process, new data is synced on a regular basis, and you'll have many tables of data to choose from.

💡 The data sync frequency is **24 hours**. You can set the daily sync time in your project settings.

Connectors are powered by our unique partnership with Fivetran. They've built an enterprise grade data integration platform that is trusted by 2000+ demanding customers. You'll interact with them in the connector authorization page.

## Google Sheets

If there's no dedicated connector, Google Sheets offers a great alternative for getting your data ready:

*   Many tools offer one-off or scheduled exports to Google Sheets
    
*   Many automation tools (Zapier, Pabbly Connect, n8n) write to Google Sheets
    
*   Typing `sheet.new` in your browser bar is the quickest way we know to quickly jot down or copy + paste data
    

Gyana has a native Google Sheets connector that will take a **few seconds** to import. Just share the sheet with us, copy and paste the URL, and you're done.

💡 By default, new data will not automatically sync from your sheet if you make changes. You need to manually re-sync. We have improvements to this planned.

💡 You can paste a Google Sheets link to any page within a Gyana project to start adding the Integration.

## Upload CSV

Your next alternative is the swiss-army knife of data, the CSV file. Nowadays, most tools (including Excel, databases, web apps, ads accounts) will export a CSV file that you can download and upload to Gyana.

Our native CSV importer is designed to handle most CSV nonsense, including quoted newlines, jagged rows and autodetecting headers. If your CSV file fails to import, you can always try uploading to Google Drive, opening as a Google Sheet, and connect to that instead.

💡 We will always autodetect the first line of the CSV as a header row.

## Custom API

The custom API is a good option import data from a web service, including internal APIs, when a connector is not available. You'll be able to automate data imports for any API, with flexible configuration options including OAuth2.

Read our custom API reference to learn more.

## Webhooks

Webhooks are a good option if your service publishes events via a webhook. You can deliver all those events as custom tables in Gyana.

💡 You can find webhooks as an option under connectors.

## Custom integrations

If you have a data source in mind, but don't see an automated way to set it up with our existing tools, **we'll build it for you in 2 weeks** as part of our paid plans. Reach out to us to learn more.

## 🔮 What does the future hold?

We know first hand the pain of duct taping tools together to move your data around. Our focus is to add seamless integration to as many data sources as possible, including webhooks, APIs and web scrapers.

Down the line, we're also exploring hosting public datasets (e.g. demographic segmentations, Google trends), and even paid datasets from partner providers. If that's something you'd be interested in trying out, please get in touch!