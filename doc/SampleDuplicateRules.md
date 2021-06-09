
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
