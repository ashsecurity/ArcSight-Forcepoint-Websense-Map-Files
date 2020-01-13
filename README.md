# Forcepoint Websense Map Files for ArcSight

These are map files for ArcSight to enrich Forcepoint Websense SWG log in ArcSight, that is sent over syslog.

I have used [Forcepoint Websense](https://www.websense.com/content/support/library/web/v84/siem/siem.pdf) version 8.4 integration guide. I think it may give you a good basis to build on top of it. 

From the ArcSight FlexConnector Developer's Guide:
>Map files are actual physical files, located in the connector itself. Map files operate on events after they are
collected and parsed, but before they are sent to the destination, conditionally changing one or more event
fields. 

Place this files into the `$ARCSIGHT\user\agent\map` folder and make sure to rename the file to map.X.properties, where X stands number, following the previous one, so that map files are named map.0.properties, map.1.properties, and so on. I usually **do not delete** default files, but rather add custom ones by increasing ordinal numbers from the last default one. 

* map.X.properties - Disposition Reference - Adding information about disposition based on received reference number
* map.X.properties - Category Reference  - Adding information about category based on received reference number
* map.X.properties - Basic Categorizer - Adding basic categorization information
* map.X.properties - Conditional Category Outcome - Based on deviceAction value adding categoryOutcome value

