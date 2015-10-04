# Docker configuration for orocrm and postgresql

The purpose of this configuration is to try orocrm at home.

It contains all fixes to run orocrm with postgresql as database. The CRM is exposed on port 81
on the docker's host. Installation of orocrm itself is not handled but all steps are prepared for it.
The only thing that is not prepared is the database password (which is ``postgres``).

## Fixes

 * The UUID extension is installed in postgresql at the first startup,
 * a patch for orocrm is executed which is required because of docker's filesystem,
 * PHP is configured with recommended settings (``memory_limit`` and ``date.timezone``).

## ToDo

 * Mail is neither configured nor tested.