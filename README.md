Getting-started-with-IBM-Monitoring-and-Analytics-for-Bluemix-Add-On
====================================================================

Getting started with IBM Monitoring and Analytics for Bluemix Add-On

Tomado de https://www.ng.bluemix.net/docs/#services/monana/index.html#gettingstartedtemplate

As a developer, your focus is on delivering new applications and updates continuously. Performance of your code is a critical factor, so having a tool that can help you optimize it can be extremely valuable, but only if it does so without taking time away from your real job. In fact, it should be saving you time.

What you need:

    It must be quick and painless to learn and deploy.
    It must run in my development, testing, and production Platform as a Service environments.
    It needs to make it easy for me to find the bottlenecks anywhere in the application.

What the Monitoring and Analytics add-on provides:

    Capabilities that are built in to the development environment so you see instant results.
    Insight into how your code might affect the performance of the application.
    Easy-to-use dashboards and integrated analytics-powered search capability help you find the root cause line of code quickly and easily.
    Integrated log file analysis on a single tab that helps you to quickly identify errors.

Monitoring and Analytics offers a service that you can learn about quickly and deploy painlessly. You can use this add-on in development, test and production Platform as a Service environments.

To add Monitoring and Analytics to an application:

    Log in to Bluemix™. From the DASHBOARD view, expand ADD-ONS, and click CONNECT AN ADD-ON.
    From the Bluemix CATALOG view, which is positioned at the group of Add-Ons for managing and monitoring applications, click the Monitoring and Analytics icon.
    Choose between the free and the diagnostic plans in the Selected Plan dialog box:

    Free
        You can use the free plan to monitor the availability of any type of application and to help you with basic monitoring and log analysis for Liberty and Node.js based applications.
    Diagnostic
        The diagnostic plan contains the same features as the free plan as well as the latest features. Choosing the diagnostic plan allows you to conduct enhanced performance monitoring for Liberty applications. The enhanced monitoring is facilitated by performance metrics that are not available in the free plan. By choosing the diagnostic plan, you are also ensuring that the latest features are available to you after each release.

    To view more information about the add-on, click VIEW DOCS.
    Select the name of your application, if not already selected, and click CREATE. The "Restart Application" dialog displays.
    As you do not need to restart your application now, click CANCEL.
    In the left navigation bar, under "Manage Spaces" and "APPS", click the name of your application. A screen displays with a Monitoring and Analytics-xxxxx icon, where xxxxx is a randomized string that Bluemix generates to uniquely identify your application instance.
    Click the Monitoring and Analytics-xxxxx icon.
    To activate the monitoring data collector, push your application again when prompted. This step is required.
    Switch to the command window where you previously issued your application cf push command, and issue the same cf push command again.
    Switch back to the Bluemix UI, and either refresh your browser or wait a few seconds for it to refresh itself. The tabbed UI view displays your application's availability and performance monitoring data.

You are now ready to use the add-on to monitor your application.

If you connect the add-on to more than one application and you delete the add-on from the application, the add-on is deleted and disconnected from all the monitored applications. To remove a specific instance of the Monitoring and Analytics add-on, disconnect it from the application instead of deleting it.
To disconnect the add-on:

    To open the application overview. click APPS and click the relevant application.
    Click the Menu icon on the Monitoring and Analytics add-on and click Disconnect Add-On.
    After you disconnect the add-on from an application, you must push your applications again to stop data collection from the disconnected application.

If you want to completely remove the add-on, you can delete it. To delete the add-on:

    Click DASHBOARD
    Click Monitoring and Analytics.
    Click the Menu icon and click Delete Add-On.
    Click OK when prompted.

If you initially choose the Free plan but later want to use the Diagnostic plan, you can switch the plan. To switch from the Free plan, you need to remove the free version and bind the add-on again as described in the previous steps, choosing Diagnostic instead of Free in the Selected Plan dialog box.
Diagnostic plan features (Diagnostic)

The availability of features for the Monitoring and Analytics add-on depends on the type of plan that you choose when you choose the add-on.

All of the features documented here are available in the free plan except for those which include (Diagnostic) in the title. These features are only available in the diagnostic plan. The diagnostic plan contains the most up to date features and developments for the add-on.
In- depth monitoring of Node.js based applications
The Diagnostic version of the add-on includes the following widgets that you can use to monitor Node.js applications in detail. You can use these widgets to get to:

    Identify request instances with the highest response time
    Retrieve contextual information about requests and methods
    View request data in a Tree view, allowing you to view a request and related requests easily.
    View the stack trace for a specific request
    Monitor the percentage of time spent working on specific requests
    View detailed time distribution information

The following widgets are only available in the Diagnostic version:

    Sampled Request Instances
    Request Context
    Method Trace
    Request Stack Trace
    Request Time Breakdown
    Request Time Distribution
    Request Summary

For more information about each widget, click the help icon on the UI.
Enhanced monitoring of Liberty based applications

The Diagnostic version also contains some additional metrics that are not part of the Free version. You can use these to get more information about Liberty based applications that you use.
Monitoring and Analytics overview

The Monitoring and Analytics user interface features tabbed views for Availability, Performance Monitoring, and Log Analysis.
Note: The Performance Monitoring and Log Analysis tabs are only displayed when you are using an application that is based on one of the compatible runtimes, either Node.js or Liberty.
Tabs overview
The Availability tab provides basic "ping" information about your Bluemix application URL. The results from recent hours are displayed so that you can answer the following questions:

    Has my Bluemix application been consistently reachable and responsive?
    Were there time periods when application response times were unusually slow?
    Were there time periods when my application was down, as signified by 404 or other non-200 status codes?

The Performance Monitoring tab provides resource metrics about your Bluemix Liberty or Node.js based application. Recent data is displayed so that you can answer the following questions:

    Any unusual spikes in CPU usage?
    How much heap memory has my application been using and is it within acceptable limits?
    What is my application's thread pool usage, and is it what I expected?
    How frequently and for what duration has garbage collection run and might that impact performance?
    What pages were the most frequent target of GET and POST requests in my Node.js application?

The Log Analysis tab provides information that helps you to search for and identify errors in the log files that are generated by the monitored applications. The features of this tab help you to complete the following tasks:

    Search all the log records.
    Filter searches by time period. The default is last day.
    Filter searches by data source. Each log type is represented by a data source, which you can search individually.
    Filter searches by keyword. The keywords are based on key fields that are returned in the search.
    Graph search results.

The Log Analysis tab

Use the Log Analysis tab to help you to search the log files that your application generated in the previous 24 hours, identify errors, and graph search results. You can also filter the results.
Searching log files

To search, type a search term and click Search. To view distribution information for all logs, type the wildcard character, an asterisk (*), in the Search field.

To search for a partial string, type an asterisk (*) at the start and end of your search string. For example, to search for strings that contain the phrase "hostname", type *hostname*.

After you click Search, the log records that contain a match for your search term are displayed. A graph that shows the distribution of matching events in the log is also displayed.

The search results timeline displays a graph that shows the distribution of log events over a time period. You can use the timeline slider to view the logs for a specific duration. You can zoom in and out to change the range of the data displayed.
Viewing search results
Log records are displayed in both in a grid view and a list view. The default view is the List view. Log records that are displayed in the grid view can be ordered by column for easy analysis. This view can be customized and used to display information in a range of ways:

Toggle views
    Click List View or Grid View button to toggle between views. In each of these views, you can use the button that is displayed to toggle to the alternative view.
Sorting in Grid view
    You can sort the information in the table columns by clicking the column header. Not all columns are sortable.

Customizing the columns that are displayed
    To configure Grid view to display only the columns that you require, click the Select Columns icon on the Grid view toolbar, remove the columns that you do not want to display, and click OK.

Graphing search results

After you complete a search, you can display search results as a chart. To display the chart, select the column and click the Plot Column icon on the Grid view toolbar. The distinct values that are used to plot the chart can be viewed as hover help for each chart sector. The Plot feature is not available for all columns. Where available, the Plot Column button is active when the columns are selected.

You can also change the settings for a chart after you create it. To change the settings for a chart, select the chart and click the Edit icon. Make your changes and click Render.
Filtering search results
You can filter search results by time, data source, or keyword.

Filter by time
    If you know when an error occurred, you can filter the search for a specific time. To filter searches for a specific time, click the time filter button that is next to the Search button and select a time period.
Filter by data source
    If you know that an error was generated in a specific type of log within the application, you can filter by data source. For example, if you are using this add-on with the Liberty-based application and you know that there are errors occurring in the messages.log file, you can filter the search so that only errors from this type of log file are displayed. To filter by data source, click the data source icon and remove the check box for the data sources that you do not want to search. All data sources are selected by default. The data sources represent different types of log files. For example, the data sources for Liberty applications include the following log types:

        Liberty
            messages.log
            trace.log
            ffdc
            http access log

Filter by keyword
    Log Analysis search results include keywords that are displayed in the pane on the left side of the UI. The keywords are based on log fields and you can use them to filter search results. To display all the log file records that match a keyword value, open the keyword node, click on a keyword value, and click Search. All the log records that contain the selected keyword value are displayed. For example, the log fields that are used as keywords for a Liberty message log file include datetime, source, severity, messageId, methodName, className, loggerName, threadId, recordHeader, and message key.

Setting the threshold for bulk message emission in Node.js based applications

If you use the add-on to analyze the logs of an application that runs in a Node.js runtime, you can use the scala_bulkMessageEmitThreshold parameter to configure the threshold for bulk message emission. The threshold is measured in bytes. The default value is 250000. After the cache of log files in the application breaches this threshold, the log files are sent to the add-on for processing.

To set this threshold manually, add the scala_bulkMessageEmitThreshold=250000 parameter to the manifest.yml file used by your application.
You can also use a command line terminal to set the threshold. For example, to set the threshold to 150000 bytes, enter the following command in the command line interface:

$ cf set-env application_name scala_bulkMessageEmitThreshold 150000

Query syntax

You can use the described combination of words, keywords, and symbols to search for phrases in the Log Analysis tab.
Standard keywords and operators

You can use the following standard keywords and operators to search log records in the Log Analysis tab.

AND
    By default all terms or expressions must be matched in the results. A variation to this keyword is and.
""
    Use to group individual terms into phrases that are searched for as a unit. For example, "document clustering".
()
    Use to group expressions to guarantee precedence. For example, document AND (cluster OR clustering).
*
    Wildcard operator that can be replaced in the returned value with a number of characters. This can be either passed as an operator to the sources or expanded when the meta.wildcard-expand option is turned on. For example, *boat might return boat or motorboat or sailboat or speedboat.
?
    Wild character operator that can be replaced in the returned value with a single character. This can be either passed as an operator to the sources or expanded when the meta.wildcard-expand option is turned on. For example, bo?t might return boat or boot.
$
    Unstemming operators. For example, boat$ might return boat or boats or boating. This can be either passed as an operator to the sources or expanded when the meta.stemexpand option is turned on.
+
    Must operator. Forces the use of a keyword. For example, Tom +and Jerry searches for strings that contain the keyword and. 
BEFORE
    The specified term or expression must appear before another term or expression in the search results. For example, BEFORE clustering. Variations to this keyword are FOLLOWEDBY and THRU.
field:
    Use to restrict your query to a specific field. For example, author:smith or title:"war and peace". These operators are activated for every field that is defined in your syntax.
    By default, the search engine supports the title field. When you are creating a search collection, you can extract any number of contents, for each document, and relate these contents to searchable fields. This is specified in the form of the source that is associated with each collection.
NEAR
    Both terms or expressions must be matched in the results and contained within a specified proximity. It can be applied to any number of sub-expressions. For example, war AND peace NEAR (novel OR book). A variation to this keyword is WITHIN X WORDS.
NOT
    The specified term or expression must not be matched in the search results. Variations to this keyword are NOT and -.
OR
    Either term or expression must be matched in the results. A variation to this keyword is or.

Extra keywords and operators

This topic lists more keywords that are more specific to the search and indexing operations that are performed by the search engine.

The search engine manipulates ranges of text. For example, the search term A AND B corresponds to all the shortest ranges of text that contain both A and B. The search term A before B corresponds to all the shortest ranges starting with A and ending with B.

Unlike the standard operators, these operators can only be interpreted in the context of manipulations of text ranges. These operators are designed for advanced users for testing the content of a collection.

CONTAINING
    Selects the ranges that are specified by an expression that contain some of the ranges that are specified by a subsequent expression. For example, (document THRU clustering) CONTAINING enterprise corresponds to minimal ranges starting with document and ending with clustering containing enterprise, CONTENT title CONTAINING enterprise corresponds to title contents containing enterprise.
    Because the search engine operates on non-nested ranges of text (document THRU clustering) CONTAINING enterprise is not the same as document THRU enterprise THRU clustering. A sequence such as "document clustering as done in enterprise search software provides an excellent example of clustering" is only matched by document THRU enterprise THRU clustering. In the first query, the initial phrase, document THRU clustering matches the text range document clustering, and not the larger text range in the expression. In the second query, document THRU enterprise matches the text range document clustering as done in enterprise, which is then be expanded by THRU clustering to include the entire expression.

CONTENT
    Selects the ranges of text corresponding to a specific content. For example, (document AND clustering) WITHIN CONTENT title retrieves instances of the terms document and clustering in the content title. Unlike the field: operator, there is no field mapping that is involved with this operator, it matches the original content name as it is indexed.

NOTCONTAINING
    The reverse of CONTAINING, selects the ranges that are specified by an expression that contain some of the ranges that are specified by a subsequent expression.

WITHIN
    The specified terms or expressions must be matched within the ranges that are specified by a subsequent expression. For example, document THRU clustering WITHIN 4 WORDS retrieves all the sequences that start with document and ending with clustering that fit within a range of four words.

NOTWITHIN
    The reverse of WITHIN, the specified terms or expressions must not be matched within the ranges that are specified by a subsequent expression.

N WORDS
    A unary operator that takes an integer argument, and returns all the sequences of words of the specified length. For example, 5 WORDS THRU clustering CONTAINING enterprise retrieves all sequences of five words that end with the word clustering and, which contain the word enterprise.

Integration of manually configured Liberty servers with Log Analysis

In most cases, when you bind the Monitoring and Analytics add-on to a Liberty application, you do not need to configure your Liberty application to collect log files because this configuration is done automatically. However, if you use a server.xml file to manually configure a Liberty application, you need to edit the file and enable binary logging before you can analyze log files on the Log Analysis tab.

    Open the server.xml file for your application.
    Add logAnalysis-1.0 in the <feature></feature> tag.
    Add the following code in the httpEndpoint tag:

    <accessLogging filepath="../../../../../logs/http_defaultEndpoint_access.log" logFormat="%h %u %t &quot;%r&quot; %s %b %D %{User-agent}i" />

    Add the <logAnalysis> tag to specify the service instance. For example:

    <logAnalysis analyticsServerAddress="${cloud.services. <service_instance_name>.connection.url}" tenantId="${cloud.services. <service_instance_name>.connection.userid}" password="${cloud.services. <service_instance_name>.connection.password}" />

    where <service_instance_name> is the name of the service that you want to bind your application to.
    To set logging properties, add the following element to the server tag:

    <logging traceSpecification="*=info" />

    To enable binary logging, add the following information to the bootstrap.properties file:

    websphere.log.provider=binaryLogging-1.0

