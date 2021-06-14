
# Sample Duplicate Rules

# Purpose of this document

Does your organization need to prevent pesky duplicates from being created?  Are the built-in duplicate and matching rules not working for your specific needs?

Are you not sure how to set up duplicate and matching rules to achieve what you need?

This document is a catalog of matching criteria that you can use if they meet your needs perfectly, or as a starting point if you want something that's very close.

# Catalog of matching criteria

## I want to check all the email fields on Contact instead of just the standard Email field, along with a fuzzy first name match and exact last name match.

First, create a matching rule for the Contact object:

![matchingruleedit](https://user-images.githubusercontent.com/251229/121421812-8dd99600-c93c-11eb-9f15-0c169ddeb72b.png)

![matchingruledetail](https://user-images.githubusercontent.com/251229/121421577-4ce18180-c93c-11eb-938a-bbbbd05d1c5a.png)

Your matching criteria should look like this:

> ((Contact: AlternateEmail EXACT MatchBlank = FALSE) OR (Contact: HomeEmail EXACT MatchBlank = FALSE) OR (Contact: WorkEmail EXACT MatchBlank = FALSE)) AND (Contact: FirstName FUZZY: FIRST NAME MatchBlank = FALSE) AND (Contact: LastName EXACT MatchBlank = FALSE)

Next, create a duplicate rule that uses your new matching rule:

![duplicateruleedit](https://user-images.githubusercontent.com/251229/121421979-bb264400-c93c-11eb-9907-95d803e296cf.png)

![duplicateruleview](https://user-images.githubusercontent.com/251229/121422081-d85b1280-c93c-11eb-8c83-129ceb7bc2c4.png)

And you're done!

## I am creating Leads, and I want to check whether my new Leads are duplicates of existing Contacts.

The out-of-the-box rule that compares Leads to Contacts has two shortcomings for organizations using NPSP or EDA:
1. It maps the Lead's Company field to the Contact's Account Name field, but NPSP and EDA generally use special Account Names
2. It doesn't know about the multiple email fields that are present, and only compares the Lead's Email field to the Contact's Email field

You can solve this problem by writing your own Contact matching rule, like we do [above](#i-want-to-check-all-the-email-fields-on-contact-instead-of-just-the-standard-email-field-along-with-a-fuzzy-first-name-match-and-exact-last-name-match), then including it in a custom duplicate for for Leads.

![leadduplicateruleview](https://user-images.githubusercontent.com/251229/121718483-5be94080-cab0-11eb-8301-c6879cefced2.png)

## Screen Flow Video

Screen Flow Example: In this case what Pranav did was he created a screen flow that finds duplicates with the flow and shows them on the contact object. You can see from the screenshot and corresponding video how the flow was created. 

In addition, we are looking to do the same thing for opportunities. In this case the flow will find a single contact and see if the contact has duplicate records in the system. And it will reparent the opportunity to the user selected contact. This will be pasted in the document later. 

Please see the link for the screen flow example. 

https://drive.google.com/file/d/1DHJ0ncg7dPNQqGhNKTsODDizc_WQKWgy/view?usp=sharing






