# Assignment 2

This application in this repository implements a simple web service which allows clients to create and read user accounts and create, read, and delete articles. Note that the database is in-memory, not persistent. You will need to update the application to do the following (be sure to follow RESTful conventions and handle edge cases with appropriate status codes, ex. 404, 400, etc.):

## Finish User Management

1. (0.5pt) PUT endpoint to update a user account
2. (1pt) DELETE endpoint to delete a user account -- make sure to cascade the delete to delete all user articles and drafts so there are no orphaned articles

## Article Draft Flow

Instead of simply updating articles, your product managers want a draft flow. Essentially, a user should be able to create a draft of their article, make changes to that draft, and then publish the draft as a new version of the article. You will need to do the following:

1. (0.25pt) Add a new field to the Article model to store the version number
2. (0.25pt) Add a new field to the Article model to store the draft status (draft, published)
3. (2.5pt) PUT endpoint to update an article draft (if the article does not have a draft, create a new draft version)
4. (2pt) GET endpoint to get an article draft or currently published version if there is no draft
5. (2.5pt) POST endpoint to publish an article draft as a new version of the article
6. (1pt) DELETE endpoint to delete an article draft or 404 if there is no draft

## Bonus

(2pt) Add tests for your new routes testing happy path and error paths.
