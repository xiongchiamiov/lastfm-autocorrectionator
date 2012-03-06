Last.fm's autocorrection has improved things, but there are still a bunch of
mistagged artists and tracks.  Enter the [Auto-Correction Brigade].

However, doing all this manually is a pain.  Enter [the batch processor][0]
([gcode]).

However, getting a Perl script to run on people's machines is a PITA, and the
track-submission process is slow and a little annoying.  Enter the
autocorrectionator.

[Auto-Correction Brigade]: http://www.last.fm/group/The+Auto-Correct+Correction+Brigade
[0]: http://www.last.fm/group/The+Auto-Correct+Correction+Brigade/forum/119632/_/522400
[gcode]: http://code.google.com/p/rowaasr13-lastfm-pl/downloads/list

# What

Some sort of web app.  People log in using their Last.fm credentials ([docs]),
then submit things in need of auto-correction voting.  In order to submit
things for help, they have to vote in some way.

If we can do this automatically, they just have to agree to let us use their
credentials to do a batch-vote every day (or whenever).  This means they don't
even have to revisit the site in order to keep helping.

If we can't do that (or they don't want to give us their password, since we
can't do voting via the API), when they submit a request we'll ask them to
submit votes on a few other requests we have in the system (via iframe?).

Preferably there'll be some sort of voting on requests to filter out poor ones.
Also, some way to mark a request as done, so we don't keep voting on it.
Alternatively, the algorithm could just be weighted towards newer requests.

Y'know, we might as well not require logins; if they're anonymous, their
requests are weighted lighter, probably limited, and we won't keep track of
which requests they've already voted on (those will be filtered out for
logged-in users).

[docs]: http://www.last.fm/api/webauth

