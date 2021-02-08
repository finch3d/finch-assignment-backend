# Backend Assignment

## Background

Finch has a domain with `user`, `organization` and `project`, which are exposed as REST apis, e.g. `/users/:userId`, `/orgs/:orgId` and `/projects/:projectId`.

Example organization
```json
{
  "id": "b03bbcc0-d693-44d9-b60c-345a88e2301c",
  "name": "Finch"
}
```

Example user
```json
{
  "id": "1843a80a-98f2-4928-8c1a-a53efe99adbe",
  "name": "Tony Stark",
}
```

Example project
```json
{
  "id": "63d8b70f-815e-474b-830b-3e96a25544e4",
  "name": "Turning Torso"
  "orgId": "b03bbcc0-d693-44d9-b60c-345a88e2301c"
}
```

Finch now needs to add better access control so that we can control what a user can do with an organization and project, e.g a user must be a member of an organization to get read access ot its projects.

## Task 1
Create an API that supports the following requirements:
* A user can be added and removed as a member of one or more organizations.
* If a user is a member, they must have one of these roles: `admin`, `member`.
* A user needs to be `admin` to modify add or remove members in an organization.
* Default organization access rights for all projects is `read` for all org members.
* Document how the `/projects` endpoint can make use the access rights, e.g. how to call a helper function.

## Task 2
* Access rights for a project can be set for a specific user.
* Possible project access rights are: `readwrite`, `read`.
* A user needs to be org admin to modify any access rights for a project.

## Task 3
* Default access rights can be set for an organization, e.g. `readwrite` or nothing.
* Default access rights can be set for a project, which overrides the default organization rights, e.g. `read` or `readwrite`.

## Instructions

* Please use Node.js create a runnable project.
* Put the code in a git repo.
* Write down thoughts on:
  * important design decisions
  * assumptions
  * things that you wanted to do but had no time to do
  * things you would do differently if this was in production
  * things you tried but did not work out
  * changes in other code/apis you would like to have
  * etc.
