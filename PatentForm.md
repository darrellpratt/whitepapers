# Invention Title
> A system to suggest characteristic clusters to an end user of a dimensional query builder to build self healing reports. Clusters of characteristics are determined based upon a common matching algorithm against a set of lowest level UPC item data. User of system is prompted to substitute the UPC data with the derived characteristic data in order to create a selection that will deliver consistent results as the low level data changes over time.

# Short Title
> A system to substitute characteristic data for low level UPC items to build self healing reports.

# Problem
> The current data selector application used within the Nielsen Buy Platform (Answers On Demand) is commonly perceived as a complicated application to use by our end users.  Most users do not understand the concept of characteristics or the arrangement of characteristics into hierarchies.  Users generally select only the lowest level of items from the selection screens and save these selections to run scheduled reports.  This selection methodology presents a problem in that the lowest level data (UPC) can change over time with changes to the IDs or additions and deletions of those data points.  If the user would instead build a selection from the characteristics that describe the low level item, this selection would create a self-healing report that would capture new items as they are added to a store or market over time and would also capture the changes to existing data.


# Inspiration
> In the process of designing a new data selector for our next release of Answers on Demand, our user experience team interviewed users of the current system and without exception, the users stated that they did not understand characteristic data in the system and generally did not use those.  It became clear that the users were not using a feature that would enable their reports to run more efficiently over time and reduce operational costs for Nielsen involved with responding to user tickets regarding changes to the data over time.

# Your Solution/Invention

> The solution to steer users toward characteristic selections in the data selection process is to create an algorithm within the application that will pull a set of common characteristics that describe an arbitrary group of low level data items. The data for this is housed in our underlying data warehouse at each low level item as a set of facets upon that item. Those facets are to be parsed and normalized upon user selection and a set of facets that describe all the various characteristics are then captured by this application. The application will then group the set of common characteristics from the data set that describe either the full list of lowest level data points or the highest number of data points and prompt the user with an option to change the selections from low level items to the characteristic set. If the user choosed the replacement characteristic set, then the low level items are replaced and the report will act as a self healing report.

> Current systems generally are explicit in the user selection or filtering process and offer little support in guiding a user toward a more intelligent data filter for a BI style report.  These tools generally just assume an advanced user is accessing the system and provide no intelligence around the actual data in the underlying system. At best, current systems might only show the characteristic data on one item from the dataset but do not try and summarize a set of those items.


#  Value To The Business 
The system described would be of value to the business as it would reduce the ongoing maintenance of reports for clients.  Generally saved reports need to be updated when data is refreshed in the system.  These events primarily are the addition and removal of this UPC data so a system which would move more reports toward capturing the characteristic data would remove a sizeable portion of maintenance work currently performed by Nielsen.


# Is the invention in a conceptual stage or a developmental stage
Conceptual stage at this moment.

# How have others, either inside or outside of Nielsen, addressed the problem(s) (if at all) and what is the present relevant commercial practice?
n/a


# What are the basic differences from and advantages over previously known or other solutions
n/a

