###################
GitHub organization
###################

This page explains how the `RITlug GitHub organization`_ is organized and how
to manage it.


*******
Purpose
*******

The GitHub organization is a central place to manage club projects, membership,
and infrastructure. Most data is static and doesn't change often. Setting up
club projects or adding a new member is when you usually need to interact with
the GitHub organization.


************
Repositories
************

There are no restrictions on repositories allowed. Repository creation
permission is granted only to eboard members as a precaution. This approach was
decided to ensure that the current eboard has a chance to review a project
before officially endorsing it underneath our GitHub organization.

Generally, repository creation should be encouraged rather than discouraged.


******************
Adding new members
******************

There is no criteria for adding new members to the RITlug GitHub organization.
In the future, if a membership criteria is developed, this section should be
updated.

Active community members of RITlug should be added to the GitHub organization.
Adding a new person to the GitHub organization validates their contributions and
activity in the club and helps others be included with projects. Past eboards
intentionally chose a loose definition of membership in GitHub for this reason.

These steps should be followed to add a new member:

#. Add them to organization via GitHub
#. File new issue in `RITlug/tasks`_ to welcome them
#. Add them to an appropriate GitHub Team (detailed below)

.. figure:: /_static/img/github-org-add-member.png
   :alt: Add a new member to the GitHub organization from the People page

   Add a new member to the GitHub organization from the People page

Welcome message
===============

To welcome a new member to GitHub and to notify them of why they were added,
file a new issue in `RITlug/tasks`_ to explain why they were added and how to
set their membership status to public. Past examples can be used as references
([#f1]_ [#f2]_ [#f3]_).

Telling the person how to set their membership as public is important. This
instruction should always be included in the welcome message.

.. [#f1] https://github.com/RITlug/history/issues/12
.. [#f2] https://github.com/RITlug/history/issues/13
.. [#f3] https://github.com/RITlug/history/issues/18


************
GitHub Teams
************

GitHub Teams are a tool to organize members inside of a GitHub organization.
This also allows for permission matrices for different repositories and
projects.

.. figure:: /_static/img/github-org-teams.png
   :alt: GitHub Teams in our organization

   GitHub Teams in our organization

There are four teams:

#. **Eboard**: Club leadership (grants admin access to all repositories)

#. **Friends of RITlug**: Active participants with the club from outside RIT or
   other friends of the club (does not include permissions)

#. **Members**: RIT students, faculty, and staff participating in RITlug (does
   not include permissions)

#. **TigerOS Team**: `TigerOS`_ project team (grants write access to TigerOS
   repositories)

Anyone added to the GitHub organization should belong to at least one team.


.. _`RITlug GitHub organization`: https://github.com/RITlug
.. _`RITlug/tasks`: https://github.com/RITlug/tasks
.. _`TigerOS`: http://tigeros.ritlug.com/
