# Widgets reference

How to use each widget in dashboards.

Our detailed guide to each widget in workflows. _Over time, we'll expand each widget into a separate page with a detailed description, visual examples, and comparison to popular BI tools._

## Text

Use the **text** widget to write explanatory notes on your dashboard.

## Table

Use the **table** widget to display raw data in a grid of rows and columns.

The dashboard user will be able to sort and paginate through the entire dataset, perform aggregation, and add formatting like currencies, percentage or positive and negative background colors.

## Column

Use the **column** widget to display **one or more** metrics against **one** dimension.

The horizontal x-axis of the chart shows the **Dimension**, and on the vertical y-axis are the **Metrics**. You need to calculate at least one metric, but you can add as many as you want.

📚 _Example: Display the CPC and CPM by acquisition channel._

## Stacked Column

Use the **stacked column** widget to display **one** metric against **_two_** dimensions.

In a stacked column chart, each of the vertical bars from a column widget is segmented by a second **Stack Dimension**.

By default, the height of each segment in the bar is the _value_ of the metric. If you choose to **Stack 100 percent**, the height of each segment is the _proportion_ of the metric.

📚 _Example: Display the CPC by acquisition channel and day of the week._

## Bar

Use the **bar** widget to display a column widget in a horizontal direction.

## Stacked Bar

Use the **stacked bar** widget to display a stacked column widget in a horizontal direction.

## Line

Use the **line** widget to display **one or more** metrics against an **ordered** dimension (e.g. date, ranking).

The horizontal x-axis of the chart shows the ordered **Dimension**, and on the vertical y-axis are the **Metrics**. You need to calculate at least one metric, but you can add as many as you want.

By default, the x-axis is ordered by the **Dimension** in ascending order. Usually, you'll want to keep it like this as in a line chart, the order of the data points represents something meaningful, like the order of time.

💡 Line charts are currently the best chart for time series data. A dedicated time series chart is coming soon.

📚 _Example: Display the CPC and CPM by week._

## Stacked Line

Use the **stacked line** widgets to display one metric grouped by a **stacked dimension** against an **ordered** dimension.

## Pie

Use the **pie** widget to display **one** metric against **one** dimension as a percentage.

Each slice of the pie shows the **Dimension**, and the size of the slice of the percentage of the metric **Metric**. You can only calculate one metric.

💡 Pie charts are most useful for a few data points with large differences in metrics. For pie charts with more slices and minor variations in the data, consider the column chart.

## Area

Use the **area** widget to display a line widget with a shaded area under the line.

## Donut

Use the **donut** widget to display a pie widget, where the slices become segments of a donut shape.

## Scatter

Use the **scatter** widget to display the **relationship** **between** **two** metrics for **one** dimension.

The horizontal x-axis of the chart shows the first **Metric**, and the vertical y-axis is the second **Metric**. Each data point on the scatter graph shows the values of the two metrics for each category in the **Dimension**.

The scatter widget is useful to find if any relationship holds between the two metrics, independently of the value of the dimension.

📚 _Example: Display the CPC versus CPM by acquisition channel to validate a correlation._

## Funnel

Use the **funnel** widget to display **multiple** metrics over the **stages of a process**.

Each segment of the funnel shows the stage, and the size of the segment is a **Metric**. By default, the stages of the funnel are ordered by the size of the metric.

📚 _Example: Display total users by the stage of an e-commerce purchasing journey._

## Pyramid

Use the **pyramid** widget to display **multiple** metrics in a **hierarchy**.

Each segment of the pyramid shows the stage in the hierarchy, and the size of the segment is a **Metric**. By default, the stages of the pyramid are ordered by the size of the metric.

💡 A pyramid widget is the reverse of a funnel widget.

## Radar

Use the **radar** widget to display **multiple** metrics, optionally against **one** dimension.

Each data point of the radar chart shows a **Metric**. If you optionally add a **Dimension**, each line represents a separate category.

💡 Radar charts are most useful to compare a large number of metrics across a handful of categories. If you only have two data metrics, consider a scatter chart. If you have a large number of categories, consider a column chart.

## Bubble

Use the **bubble** widget to display the relationship between **three** metrics for **one** dimension.

In a bubble chart, each of the data points from a scatter widget has a size determined by the value of a third metric (**Size Dimension**).

## Heatmap

Use the **heatmap** widget to display **one** metric against **two** dimensions, in a grid of rows and columns.

The rows and columns of the table show the two **Dimensions**, and the value and coloring represents the **Metric**.

💡 The heatmap widget is like a pivot table with conditional formatting.

## Metric

A **metric** widget displays a single numeric value derived from an aggregation. They can be useful to show key insights like KPIs. If your page has a date range control or you added a date range to the widget itself you can select **Compare to previous period** to enable percentage change indicator. Click **Positive decrease** to display a reduction as positive.

## Gauge

The **gauge** metric is perfect for showing percental progress in an intuitive manner. Simply provide a number or aggregation in percent and voíla!

## Timeseries

Timeseries charts are optimized for working with time data like stock prices. The dimension should always be a time, date or datetime column. Timeseries charts allow you to zoom into particular time frames and bin the data accordingly when getting a high-level view. Currently, we support:

*   Line and stacked lines
    
*   Column and stacked columns
    
*   Area
    

## Combination Charts

Combination charts allow you to combine line, column, and area charts into a single widget. First, select the _dimension_ you want to plot on the X-Axis. All charts will use this as reference. Then add a chart of your choice and select the metric you want to display. You can select the secondary Y-axis checkbox to plot a chart on the right Y-axis.

We recommend using not more than three different charts per widget to convey a clear and easily to understandable message.

  

## URL Embed

Use the URL embed widget to insert website embeds into your dashboards.

You might find some websites limit domains they are able to embed to, if this is the case you can either reach out the administrator of the website to whitelist Gyana or if you own the website configure it yourself.

## Image

Upload image files to your dashboard to decorate it or provide visual information.

## Date range control

The **Date range control** widget enables you to filter selected charts by the same date range. Simply drag the widget onto your page select a preset period or select **Custom** and provide a **Start** and/or **End** date. All widgets that have a **Date range column** on the current page will update accordingly.

