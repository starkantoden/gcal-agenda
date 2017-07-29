About
-----

gcal-agenda is a series of two scripts which can be used to display an
aggregated agenda for multiple calendars on your Google account.

Usage
-----

As fetching events from Google's servers can take some time, the
sync-calendars script is used to cache your calendars locally, while the
actual agenda script displays the agenda for a given number of days.

In order for this tool to work, you will need the [Google command-line access
tool](http://code.google.com/p/googlecl) installed somewhere on your system.

You should then modify the cache directory variable in both the sync-calendars
and agenda script, as well as the list of calendars to fetch in the agenda
script. Note that you will need to authorize the Google CLI tool to access
your account. This can be done by running the following command:

    google calendar list

The tool should then prompt you for authorization. Once this is configured,
set up sync-calendars to run periodically from cron. The agenda tool only
reads the cached files, so it can be run whenever you like.

"Screenshots"
-------------

With no arguments, agenda prints out 3 days of your calendars in advance,
like so:

    Today:
    - Movie with Betty @ 20:30
    Saturday:
    - Party at John's house @ 21:00
    * Some all-day event
    Sunday: No events

The agenda script also takes a single argument for the number of days to print
out. Beyond 5 days in the future, dates are printed out instead of weekday
names.

License
-------

gcal-agenda is made available under the BSD license. See the file LICENSE.txt
for more details.
