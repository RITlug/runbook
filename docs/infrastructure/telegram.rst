########
Telegram
########

`Telegram <https://telegram.org/>`__ is a messaging client similar to WhatsApp, GroupMe, Messenger, etc.
This document explains the infrastructure and management of the RITlug Telegram group, `@ritlug`_.

.. figure:: /_static/img/telegram/telegram-group-overview.png
   :alt: Screenshot of the @ritlug Telegram group

   Screenshot of the `@ritlug`_ Telegram group


**********
Background
**********

Today, the Telegram group is left online as a convenience to older members who choose to use it.
However, it is not officially advertised or endorsed by RITlug eboard.

Before switching to Slack, RITlug advertised a Telegram group and :doc:`IRC channel <irc-channel>`.
After switching to Slack and setting up a bridge, RITlug only advertised the Slack.
However, the Telegram group and IRC channel were kept online for convenience.
The work to maintain a bridge across all groups was simple: run a bot and forget.
Since this is easy to maintain, we chose to support the bridge.

Teleirc bridge
==============

The IRC bridge uses `RITlug/teleirc <https://github.com/RITlug/teleirc>`__ to run the bridge.
This service is run off of RITlug infrastructure.
See documentation for the Teleirc bridges for more information.

.. note::

   Once Teleirc bridge documentation is written, a cross-document link should be added to this section.


*****************
Moderation policy
*****************

RIT and RITlug club policy determine moderation policies.
This document is not a policy document, so it is not covered.

.. note::

   Once available, a link to those public policy documents should go here.


********************
Administrator action
********************

.. warning::
   The following instructions are shown on the official `Telegram Desktop <https://desktop.telegram.org/>`__ application.
   If you are using another platform (iOS, Android, web, etc.), the instructions may differ.

There are two types of administrator actions: **updating administrator list** and **taking moderation action**.

Update administrator list
=========================

Existing administrators with the correct permission can add other administrators.
See the :ref:`administrator-list` for a list of existing administrators.

Follow these steps to add a `@ritlug`_ new administrator.

.. figure:: /_static/img/telegram/telegram-add-admin-01.png
   :alt: Open the group overview, then click the three-prong button towards the top right to open "Manage group"

   Open the group overview, then click the three-prong button towards the top right to open "**Manage group**"

.. figure:: /_static/img/telegram/telegram-add-admin-02.png
   :alt: Open the Administrators menu, click Add Administrator button in bottom-left corner

   Open the **Administrators** menu, click **Add Administrator** button in bottom-left corner

.. figure:: /_static/img/telegram/telegram-add-admin-03.png
   :alt: Search for a new administrator by their Telegram username

   Search for a new administrator by their Telegram username

.. figure:: /_static/img/telegram/telegram-add-admin-04.png
   :alt: Select permissions to grant user (past precedent is current eboard receives all)

   Select permissions to grant user (past precedent is current eboard receives all)

Take moderation action
======================

If you need to take moderation action (e.g. banning a user or deleting spam messages), use Telegram moderation tools.
The quickest way to open the moderation tools is by right-clicking or long-pressing on a specific message in Telegram.
If these options do not appear, try deleting the message first.
If successful, an interface appears with three options to enable:

.. figure:: /_static/img/telegram/telegram-moderation-01.png
   :alt: Options to enable when deleting a message: ban user, report as spam, delete all messages from user

   Options to enable when deleting a message: ban user, report as spam, delete all messages from user [#]_

.. _administrator-list:

******************
Administrator list
******************

* Mark Repka (@Repkam09) (**creator**) [#]_
* Nate Levesque (@thenaterhood)
* Solomon Rubin (@Serubin)
* Tim Zabel (@Tjzabel21)
* Christian Martin (@ctmartin)
* Josh Bicking (@jibby0)
* Ian Flournoy (@icflournoy)

.. [#] Be careful about IRC spam – if you ban from the IRC spam messages, you may disable or ban the IRC bridge.
       Only delete individual messages or bulk-delete.
.. [#] *Creator* status is equivalent to super admin - this admin can update privileges for all other administrators.

.. _@ritlug: https://t.me/ritlug
