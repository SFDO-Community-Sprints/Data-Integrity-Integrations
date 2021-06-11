
# Initial Topic Brainstorm

# 2021-06-09

At the first breakout of the June 9-10, 2021 sprint, the team brainstormed briefly on topics relating to integrations and data integrity.  Many of these are about specific integrations, and others are about strategies for reducing data integrity problems.

Here is the list, very slightly edited, in case it's useful to a future sprint team.

* Wordpress - Salesforce 
* Excel - Salesforce 
* Oracle - Salesforce 
* Access - Salesforce
* SAP - Salesforce
* Docusign - Salesforce
* Microsoft Outlook - Salesforce
* Slack - Salesforce 
* G-suite - Salesforce
* Google Maps API - Salesforce
* Zapier 
* Duplicates from CC merchant 
* Duplicates/bad address from Events app
* Mulesoft
* [IFTT](https://ifttt.com/)
* Campaign Monitor - duplicates with email match/NPSP multiple emails.  Subscription tracking issues.
* It is my understanding that CM matches on Email field only.  So duplicates can occur if multiple email addresses are on a Contact record.
* GoToWebinar - Salesforce
* Pardot duplicates - allows for multiple prospects with the same email address that can be synced with Salesforce.
* Donations platform where integration uses Salesforce native duplicate/matching rules but names fuzzy logic isn’t followed
* How not overwrite Addresses with incomplete Addresses - so we dont get city state mismatch to the street address.  And/or overwrite Primary Address or switch Primary Address.
* Best way to match when using multiple email addresses - suggestion: use a matching rule to compare all three emails fields available in Salesforce
* And stop switching the Primary Email address.
* Soapbox - donation payment creates a new opportunity record when one already exists.  Need to manually reconcile
* Zoom integration creates lead if cannot match existing contact, duplicates
