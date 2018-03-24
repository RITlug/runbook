The RITlug IRC Channel
======================

Overview
--------

RITlug maintains an IRC channel on Freenode, which is open to the public.
RITlug members are free to discuss any topic in the IRC channel, although it is expected that discussion adheres to RIT and Freenode policies (academic dishonesty, slander, threats, or anything else deemed inappropriate by club leadership may result in a warning or a ban at the discretion of the Op(s))

The IRC channel is available on Freenode as #ritlug.
If you're not familiar with Freenode and/or IRC, you may want to brush up on your IRC basics. Here's a few things to get you started:

1. Connect to Freenode using the client of your choosing (IRSSI, Pidgin, etc)

-  Server: irc.freenode.net
-  Username: Whatever you go by!
-  Protocol: IRC
-  Password: None

2. Set your nick (May not be necessary if you set a username in your client)

-  ``/nick <your new name>``

3. Register your Nick (required if you will have Op privileges, highly recommended otherwise)

-  ``/msg NickServ register <Your Email> <Your Password>``
-  NickServ will email you a confirmation code

4. Join the RITlug channel: ``/join #ritlug``

Other commands are detailed in the sections below.

Adding a new Op
---------------

*This requires you to already have Op privileges*

As an Op, you can modify the permissions of other Ops (assuming you have permission to do so) so you can granularly control access if necessary.

After signing in and identifying with NickServ (you will be prompted)

::

    /msg ChanServ #ritlug add <username to add> +AOfiorstv

The flags (letters following the +) are detailed in `Flags <#flags>`__.
You can add or remove flags as necessary in the command depending on the access you want to grant. Some flags can't be granted due to permissions, such as Founder.

For removing an Op, scroll down to Managing Access.

Checking Access
---------------

ChanServ allows you to check (if you have permissions to do so) who has what access to the channel.

::

    /msg ChanServ access #ritlug list

or with

::

    /msg ChanServ access #ritlug info <user to check>

Managing Access
---------------

You can update a user's access levels after adding them, as necessary.
You MUST add the user, as described in Adding a New Op above, or the permissions you grant will only be temporary.
Access levels are controlled using what are referred to as `Flags <#flags>`__.

Adding permissions to a user

::

    /msg ChanServ flags #ritlug <user to change> +<your flags to add>

Removing permissions from a user

::

    /msg ChanServ flags #ritlug <user to change> -<your flags to add>

*(note the +/- in the commands above)*

You can add and remove multiple flags at a time by tacking them onto the command, for example

::

    /msg ChanServ flags #ritlug <user to change> +Afi

or by using wildcards (\*), for example

::

    /msg ChanServ flags #ritlug <user to change> -*

Removing a user from the access list (removing all their permissions as well)

::

    /msg ChanServ access #ritlug del <user to remove>

Flags
-----

Flags are used to grant and revoke access on the channel.

.. raw:: html

   <pre>
   Flag    Description
   +v  Enables use of the voice/devoice commands.
   +V  Enables automatic voicing.
   +o  Enables the use of the op/deop commands.
   +O  Enables automatic op
   +s  Enables the use of the SET command
   +i  Enables use of the INVITE and GETKEY commands.
   +r  Enables use of the KICK, KICKBAN, BAN and UNBAN commands.
   +R  Enables use of the RECOVER and CLEAR commands.
   +f  Enables modification of channel access lists.
   +t  Enables use of the TOPIC and TOPICAPPEND and TOPICPREPEND commands.
   +A  Enables viewing of channel access lists.
   +S  Marks the user as a SUCCESSOR.
   +F  Grants full founder access.
   +b  Enables automatic kickban.
   +e  Exempts from +b and enables unbanning self.
   </pre>

Handling Problem Users
----------------------

Problem users may include users who are frequently disruptive, rude, or engage in activities that RIT and/or Freenode do not approve of.
If a user becomes a problem, they should be warned and reminded of the channel policies.
If they are a problem repeatedly, then additional action should be taken.
As a reminder, RIT policies apply to all students whether or not they are on campus at the time of the offense, if it is against another RIT student or RIT.

It can sometimes be difficult to identify users in IRC.
If their real life identity is known and they are a current RIT student or faculty and they repeatedly violate RIT policies, they should be reported to the proper RIT authorities (Public Safety, Student Conduct, or for cases of academic dishonesty, their department).

Problem users in IRC can be kicked from the channel by doing

::

    /kick <problem user>

Repeatedly problematic users can be banned from the channel by name or by hostmask by doing

::

    /msg ChanServ akick #ritlug add <problem user OR hostmask>

You can also specify a reason for the ban by adding it to the end of the command. Bans can expire after a period of time or can be permanent:

::

    /msg ChanServ akick #ritlug add <problem user> !P You are banned permamently
    /msg ChanServ akick #ritlug add <problem user> !T 5d You are banned for 5 days

You can view the list of banned users with

::

    /msg ChanServ akick #ritlug list

And you can unban a user by running

::

    /msg ChanServ akick #ritlug del <no longer problem user>
