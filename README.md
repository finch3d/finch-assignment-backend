# Backend Assignment

## Background

Today Finch has a domain with users and organizations exposed through a REST api, e.g. `/users/:userId` and `/orgs/:orgId`.

Example user
```json
{
  "id": "1843a80a-98f2-4928-8c1a-a53efe99adbe",
  "name": "Tony Stark",
}
```

Example organization
```json
{
  "id": "c0ac0536-3436-4992-bf27-fb2c0d17b20c",
  "name": "Acme",
}
```

Finch now wants add the possiblity for a user to be a member of an organization.

## Task

Create an API that supports the following requirements: 
* A user can be added and removed as a member of one or more organizations.
* A member must have one of these roles: `admin`, `member`.
* A user needs to be `admin` to modify add or remove members in an organization.
* An organization must have at least one admin.

NOTE: 
* Creating users and organizations is outside the scope of this task.

## Instructions

* Create a runnable Node.js project.
* Use Docker if you want to add any database.
* Put all of it in a git repo, with instructions on how to run.
* Write down thoughts on:
  * important design decisions
  * assumptions
  * things that you wanted to do but had no time to do
  * things you would do differently if this was in production
  * things you tried but did not work out
  * changes in other code/apis you would like to have
  * etc.
