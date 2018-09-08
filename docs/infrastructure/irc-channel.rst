###########
IRC channel
###########

The purpose of this document is to inform and instruct how to manage the RITlug IRC channel on the Freenode IRC servers.


********
Overview
********

RITlug maintains a public IRC channel on Freenode.
The channel is available on `Freenode`_ as ``#ritlug``.
Additionally, it is bridged to the ``#general`` channel on Slack.
Interactions and behavior for IRC adhere to all existing university and club policies.
These policies are not defined in this document.


********************
Join the IRC channel
********************

Riot
====

For more information about using Riot as an IRC client, read this article on `how to use Riot for IRC <https://opensource.com/article/17/5/introducing-riot-IRC>`__.

Web chat
========

A short-term chat session in your browser is possible.
You will only remain connected as long as you are online.
Join the channel via the `Freenode web chat bridge <https://webchat.freenode.net/?channels=ritlug>`__.

IRC client
==========

These instructions apply if you are using a more traditional IRC client.

1. Connect to Freenode using the client of your choosing (IRSSI, HexChat, Pidgin, etc)

- **Server**: irc.freenode.net
- **Username**: preferred public username in chat
- **Protocol**: IRC
- **Password**: None

2. Register your nick, or username, with NickServ (required for operator privileges, highly recommended for all)

- ``/query NickServ register <your email> <your password>``
- NickServ emails a confirmation code

3. Join the RITlug channel: ``/join #ritlug``


******************
Add a new operator
******************

An operator is IRC lingo for a channel administrator.
An operator can kick, quiet, and ban other users in the channel.
They also have other permissions, like changing the channel's topic and adjusting other channel metadata.
New operators may only be added by current operators.

First, sign in to IRC and ensure you identify your username with NickServ.
After, run the following command to add a new operator::

    /query ChanServ ACCESS #ritlug ADD <Freenode username> +AORfiorstv

The flags (letters following the ``+``) are detailed in `Flags <#flags>`__.
Some flags can't be granted due to permissions, such as Founder.


********************
Check channel access
********************

ChanServ allows you to check (if you have permissions) who has what access to the channel.
Run either of the following commands to see the access list for the entire channel or for a specific user::

    /query ChanServ ACCESS #ritlug LIST
    /query ChanServ ACCESS #ritlug INFO <user to check>


*************************************
Manage channel access and permissions
*************************************

You can update a user's access levels after adding them via ChanServ.
Access levels are controlled using `flags <#flags>`__.

Add permissions to user
=======================

::

    /query ChanServ ACCESS #ritlug ADD <Freenode username> +<your flags to add>

You can add or remove multiple flags at once by appending them::

    /query ChanServ ACCESS #ritlug ADD <Freenode username> +Vv

Remove permissions from user
============================

Remove a user from the access list and all of their permissions::

    /query ChanServ ACCESS #ritlug DEL <Freenode username>


*****
Flags
*****

Flags grant and revoke access to the channel.

.. raw:: html

   <pre>
   Flag     Description
   +v       Enables use of the voice/devoice commands.
   +V       Enables automatic voicing.
   +o       Enables the use of the op/deop commands.
   +O       Enables automatic op
   +s       Enables the use of the SET command
   +i       Enables use of the INVITE and GETKEY commands.
   +r       Enables use of the KICK, KICKBAN, BAN and UNBAN commands.
   +R       Enables use of the RECOVER and CLEAR commands.
   +f       Enables modification of channel access lists.
   +t       Enables use of the TOPIC and TOPICAPPEND and TOPICPREPEND commands.
   +A       Enables viewing of channel access lists.
   +S       Marks the user as a SUCCESSOR.
   +F       Grants full founder access.
   +b       Enables automatic kickban.
   +e       Exempts from +b and enables unbanning self.
   </pre>


**************************
How to respond to conflict
**************************

This section explains how to respond to conflict in the IRC channel.
Sometimes it may be from club members.
More likely, it will be from spammers or groups not associated with RIT.

For RIT students, faculty, and staff, their behavior in the channel is governed by RIT and RITlug club policy.
Policy is not defined in this document.
As a reminder, RIT policies apply to all students whether or not they are on campus at the time of the offense, if it is against another RIT student or RIT.

It can sometimes be difficult to identify users in IRC.
If their real life identity is known and they are a current RIT student or faculty and they repeatedly violate RIT policies, they should be reported to the proper RIT authorities (Public Safety, Student Conduct, or for cases of academic dishonesty, their department).

Kick out a user
===============

Kick out a user from the IRC channel with this command::

    /kick <username>

Kick and permanently ban a user
===============================

If a kick does not end the conflict, a user may be banned from the channel.
When banning a user, IRC does not typically remove them from the channel.
The recommended action is issuing a **kick-ban**.
The following command kicks out and bans someone from the channel by their name or `hostmask <http://www.geekshed.net/2012/03/what-is-a-hostmask/>`__::

    /query ChanServ akick #ritlug ADD <username OR hostmask>

It is recommended to add a reason to a ban for archive purposes.
Append a reason to a permanent ban with this command::

    /query ChanServ akick #ritlug ADD <username OR hostmask> !P Permanently banned for harassing other RITlug members

Kick and temporarily ban a user
===============================

Set a ban with a time expiration with this command::

    /query ChanServ akick #ritlug ADD <username OR hostmask> !T 5d Banned for five days: Rude behavior towards others

List all banned users
=====================

::

    /query ChanServ akick #ritlug LIST

Unban a user
============

::

    /query ChanServ akick #ritlug DEL <username OR hostmask>


*********************
Channel configuration
*********************

.. note::

   This section will explain how the channel is configured, in light of the August 2018 Freenode spam attacks.
   It will be added soon.


.. _Freenode: https://freenode.net/
