# Sample Duplicate Rules

# Purpose of this document

Does your organization need to prevent pesky duplicates from being created?  Are the built-in duplicate and matching rules not working for your specific needs?

Are you not sure how to set up duplicate and matching rules to achieve what you need?

This document is a catalog of matching criteria that you can use if they meet your needs perfectly, or as a starting point if you want something that's very close.

# Catalog of matching criteria

## I want to check all the email fields on Contact instead of just the standard Email field, along with a fuzzy first name match and exact last name match.

First, create a matching rule for the Contact object:

Matching rule edit screen placeholder, before save

Matching rule view placeholder, after save

Your matching criteria should look like this:

> (Contact: FirstNameFUZZY: FIRST NAMEMatchBlank = FALSE) AND (Contact: LastNameEXACTMatchBlank = FALSE) AND ((Contact: HomeEmailEXACTMatchBlank = FALSE) OR (Contact: WorkEmailEXACTMatchBlank = FALSE) OR (Contact: AlternateEmailEXACTMatchBlank = FALSE))

Next, create a duplicate rule that uses your new matching rule:

Duplicate rule edit screen placeholder, before save

Duplicate rule view placeholder, after save


