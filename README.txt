README for inxi - a command line system information tool

The new Perl inxi is now here! File all issue reports with the master
branch.

=====================================================================
MASTER GIT BRANCH:

This is the only supported branch, and the current latest commit is
the only supported 'release'. There are no, and never will be,
any 'releases' of inxi beyond the current commit to master.

git clone https://github.com/smxi/inxi --branch master --single-branch

OR direct fast and easy install:
wget -Nc https://github.com/smxi/inxi/raw/master/inxi

OR easy to remember shortcut (which redirects to github):
wget -Nc https://smxi.org/inxi

NOTE: I have deleted the master-plain branch  to avoid confusion 
since I've removed the legacy .gz files from the branch, which were 
the only reasons for its existence.

I auto tag commits that I feel are somewhat complete at that stage
of the coding. There are NO releases, don't even dream of pretending 
a tagged release holds any significance at all. I only added auto 
tagging to get the maintainers to stop annoying me about tagging. 
There is NO repeat NO meaning to the fact a commit is tagged. A tag 
is a pointer to a commit, and has no further meaning.

Every current commit is the active release, all past commits are not 
supported. Tagging has ZERO meaning, it's purely a formality that 
certain distros can't figure out how to do without, that's all.

NOTE: JUST BECAUSE GITHUB CALLS MY TAGGED COMMITS 'RELEASES' DOES 
NOT REPEAT NOT MEAN THEY ARE RELEASES!!! I can't change the words 
on the tag page. They are tagged commmits, period. I did not want 
to use tags precisely to avoid the idea that inxi has any release 
that exists that is other than it's current master version, but I 
decided that it was less pain to add tags than to argue this point 
any further.

=====================================================================
DEVELOPMENT BRANCH:
All active development is now done on the inxi-perl branch (pinxi):

git clone https://github.com/smxi/inxi --branch inxi-perl --single-branch

OR direct fast and easy install:
wget -Nc https://github.com/smxi/inxi/raw/inxi-perl/pinxi

OR easy to remember shortcut (which redirects to github):
wget -Nc https://smxi.org/pinxi

Once new features have been debugged, tested, and are stable, they 
will move to the master branch.

=====================================================================
LEGACY BRANCH:
If you'd like to look at or check out the Gawk/Bash version of inxi, 
you can find it here, at the inxi-legacy branch (binxi):

git clone https://github.com/smxi/inxi --branch inxi-legacy --single-branch

OR direct fast and easy install:
wget -Nc https://github.com/smxi/inxi/raw/inxi-legacy/binxi

OR easy to remember shortcut (which redirects to github):
wget -Nc https://smxi.org/binxi

This version will not be maintained, and it's unlikely that I will 
spend any time on it in the future, but it is there in case it's of
use or interest to anyone.

=====================================================================
SUPPORT INFO:

Do not ask for basic help that reading the inxi -h / --help menus, or 
man page would show you, and do not ask for features to be added that
inxi already has. Also do not ask for support if your distro refuses to
update its inxi version, some are bad about that.

DOCUMENTATION: http://smxi.org/docs/inxi.htm 
(smxi.org/docs/ is easier to remember, and is one click away from inxi.htm)
The one page wiki on github is only a pointer to the real resources.

HTML MAN PAGE: http://smxi.org/docs/inxi-man.htm 
INXI OPTIONS: http://smxi.org/docs/inxi-options.htm 
NOTE: These may not always be up to date.

ISSUES: https://github.com/smxi/inxi/issues
No issues accepted for non current inxi releases. See below for more on that.

SUPPORT FORUMS: http://techpatterns.com/forums/forum-33.html
This is the best place to place support issues that may be complicated.

If you are developer, use:
DEVELOPER FORUMS: http://techpatterns.com/forums/forum-32.html

SOURCE VERSION CONTROL: https://github.com/smxi/inxi
MAIN BRANCH: master
DEVELOPMENT BRANCHES: inxi-perl, one, two, three, android.
Dev branches are rarely used, but that's where the really hard new features etc
are debugged and worked out. inxi itself has the built in feature to be able
to update itself from anywhere, including these branches, which is very useful
for development and debugging on many user systems.

PULL REQUESTS: Please talk to me before starting to work on any patch, unless
it's a trivial bug fix. Please: NEVER even think about looking at or using previous 
inxi commits, previous to the current one, as a base for a patch. If you do, 
your patch / pull request will probably be rejected.

inxi has one and only one release, and that is the current one (plus dev releases,
of course, but those should never be packaged). All previous releases are 
immediately obsolete on the commit of every new release. There is no exception to 
this, and never will be.

Man page updates, doc page updates, etc, of course, are easy and will probably
be accepted, as long as they are done according to the requirements. 

inxi releases early, and releases often, when under development. 

=====================================================================
ABOUT INXI - CORE COMMITMENT TO LONG TERM STABILITY

inxi is a command line system information tool. It was forked from the ancient
and mindbendingly perverse yet ingenius infobash, by locsmif. 

That was a buggy, impossible to update or maintain piece of software, so the
fork fixed those core issues, and made it flexible enough to expand the 
utility of the original ideas. Locmsif has given his thumbs up to inxi, so 
don't be fooled by legacy infobash stuff you may see out there.

inxi is lower case, except when I create a text header here in a file like 
this, but it's always lower case. Sometimes to follow convention I will use
upper case inxi to start a sentence, but i find it a bad idea since 
invariably, someone will repeat that and type it in as the command name, then
someone will copy that, and complain that the command: Inxi doesn't exist...

The primary purpose of inxi is for support, and sys admin use. inxi is used
widely for forum and IRC support, which is I believe it's most common function.

If you are piping output to paste or post (or writing to file), inxi now 
automatically turns off color codes, so the old suggestion to use -c 0 to 
turn off colors is no longer required.

inxi should always show you your current system state, as far as possible, 
and should be more reliable than your own beliefs about what is in your system, 
ideally. In other words, the goal in inxi is to have it be right more than it 
is wrong about any system that it runs on. And not to rely on non current system
state data if at all possible. Some things, like memory/ram data, rely on
radically unreliable system self reporting based on OEM filling out data
correctly, which doesn't often happen, so in those cases, you want to 
confirm things like ram capacity with a reputable hardware source, like
crucial.com, which has the best ram hardware tool I know of.

The core mission of inxi is to always work on all systems all the time. 
Well, all linux systems with the core tools inxi requires to operate
installed. Ie, not android, yet. What this means is this: you can have a 10 
year old box, or probably 15, not sure, and you can install today's inxi on 
it, and it will run. It won't run fast, but it will run. I test inxi on a 
200 MHz  laptop from about 1998 to keep it honest. That's also what was 
used to optimize the code at some points, since differences appear as seconds,
not 10ths or 100ths of seconds on old systems like that.

inxi is being written, and tested, on Perl as old as 5.08, and will work on
any system that runs Perl 5.08 or later. Pre 3.0.0 Gawk/Bash inxi will also run 
on any system no matter how old, within reason, so there should be no difference.

=====================================================================
BSD SUPPORT

BSD support is not as complete as GNU/Linux support due to the fact some of
the data simply is not available, or is structured in a way that makes it 
unique to each BSD. This fragmentation makes supporting BSDs far more difficult
than it should be in the 21st century. The BSD support in inxi is an ongoing
process, with more features being added as new data sources and types are 
discovered.

All BSD issue reports unless trivial and obvious will require 1 of two things:

1. a full --debug 21 data dump so I don't have to spend days trying to get 
the information I need to resolve the issue file by painful file from the 
issue poster.

2. direct ssh access to at least a comparable live BSD version, that is, if
the issue is on a laptop, access has to be granted to the laptop, or a similar 
one. 

2 is far preferred because in terms of my finite time on this planet of ours, 
the fact is, if I don't have direct (or SSH) access, I can't get much done, 
and the little I can get done will take 10 to 1000x longer than it should. 
That's my time spent (and sadly, with BSDs, largely lost), not yours. 

I decided I have to adopt this much more strict policy with BSDs after wasting 
untold hours on trying to get good BSD support, only to see that support break 
a few years down the road as the data inxi relied in changed structure or syntax,
or the tools changed, or whatever else makes the BSDs such a challenge to support.
In the end, I realized, the only BSDs that are well supported are ones that I have 
had direct access to for bebugging and testing. 

I will always accept patches that are well done, if they do not break GNU/Linux, 
and extend BSD support, or add new BSD features, and aren't too long. inxi sets 
initial internal flags to identify that it is a BSD system vs a GNU/Linux system, 
and preloads some data structures for BSD use, so make sure you understand what
inxi is doing before you get into it.

inxi will also start on Darwin, OSX's mutated version of a BSD, but my 
conclusion about Darwin is that it is Unix in name only, and I will not spend 
a second of my time adding any further support for that crippled broken 
corporate pseudo-unix system. Don't ask, unless you are willing to pay my
normal professional wages to get that support made.

=====================================================================
INXI FEATURES AND FUNCTIONALITY

inxi's functionality continues to grow over time, but it's also important
to understand that each core new feature usually requires about 30 days work
to get it stable. So new features are not trivial things, nor is it acceptable
to submit a patch that works only on your personal system. One inxi feature
(-s, sensors data), took about 2 hours to get working in the alpha test on the
local dev system, but then to handle the massive chaos that is actual user
sensors output and system variations, it took several rewrites and about 30
days to get somewhat reliable for about 98% or so of inxi users. So if your
patch is rejected, it's likely because you have not thought it through 
adequately, have not done adequate testing cross system and platform, etc.

=====================================================================
INXI RELEASE/SUPPORT/ISSUES/BUGS INFORMATION:

Important: the only version of inxi that is supported is the latest current 
master branch release. No issue reports or bug reports will be accepted for 
anything other than current master branch. No merges, attempts to patch old code
from old releases, will be considered or accepted. If you are not updated to
the latest inxi, do not file a bug report since it's probably been fixed ages
ago. If your distro isn't packaging a current inxi, then file a bug report 
with them, not here. The only valid working code base for inxi is the current 
release of inxi. 

Distributions should never feel any advantage comes from using old inxi 
releases because inxi has as a core promise to you, the end user, that it 
will NEVER require new tools to run. New tools may be required for a new
feature, but that will always be handled internally by inxi, and will not cause
any operational failures. This is a promise, and I will never as long as I run
this project violate that core inxi requirement. Old inxi is NOT more stable 
than current inxi, it's just old, and lacking in bug fixes and features.

inxi is a rolling release codebase, just like Debian Sid, Gentoo, or Arch 
Linux are rolling release GNU/Linux distributions, with no 'release points'.

Your distro not updating inxi ever, then failing to show something that is
fixed in current inxi is not a bug, and please do not post it here. File 
the issue with your distro, not here. Updating inxi in a package pool will 
NEVER make anything break or fail, period. It has no version based 
dependencies, just software, like Perl 5.xx, lspci, etc. There is never a valid 
reason to not update inxi in a package pool of any distro in the world (with
one single known exception, the Slackware based Puppy Linux release, which 
ships without the full Perl language. The Debian based one works fine).

Sys Admin type inxi users always get the first level of support. ie, convince 
us you run real systems and networks, and your issue shoots to the top of 
the line. As do any real bugs. Failure to supply requested debugger data 
will lead to a distinct lack of interest on our part to help you with a 
bug. ie, saying, oh, x doesn't work, doesn't cut it, unless it's obvious why. 

=====================================================================

INXI VERSION NUMBERING:

inxi uses fairly classic version numbering, where the version numbers actually
mean something.

The version number follows these guidelines:
Using example 3.2.28-6

The first digit(s), "3", is a major version, and almost never changes. Only 
a huge milestone, or if inxi reaches 3.9.xx, when it will simply move up to 
4.0.0 just to keep it clean, would cause a change. 

The second digit(s), "2", means a new real feature has been added. Not a 
tweaked existing feature, an actual new feature, which usually also has a new 
argument option letter attached. The second number goes from 0 to 9, and then
rolls over the first after 9. It could also be adding a very complicated 
expansion of existing features, like Wayland. It depends.

The third, "28", is for everything small, can cover bug fixes, tweaks to 
existing features to add support for something, pretty much anything where you
want the end user to know that they are not up to date. The third goes from 0 
to 99, then rolls over the second.

The fourth, "6", is extra information about certain types of inxi updates. 
I don't usually use this last one in master branch, but you will see it 
in branches one,two, inxi-perl, inxi-legacy since that is used to confirm 
remote test system patch version updates.

The fourth number, when used, will be alpha-numeric, a common version would be,
in say, branch one: 2.2.28-b1-02, in other words, a branch 1 release, version 2.

In the past, now and then the 4th, or 'patch', number, was used in trunk/master
branches of inxi, but I've pretty much stopped doing that because it's confusing.

inxi does not use the fiction of date based versioning because that imparts no
useful information to the end user, when you look at say, 2.2.28, and you last
had 2.2.11, you can know with some certainty that inxi has no major new 
features, just fine tunings and bug fixes. And if you see one with 2.3.2, you 
will know that there is a new feature, almost, but not always, linked to one 
or more new line output items. Sometimes a fine tuning can be quite 
significant, sometimes it's a one line code fix. 

A move to a new full version number, like the rewrite of inxi to Perl, would 
reflect in first version say, 2.9.01, then after a period of testing, where 
most little glitches are fixed, a move to 3.0.0. These almost never happen. 
I do not expect for example version 4.0 to ever happen after the 3.0 release 
of early 2018, unless so many new features are added that it actually hits 3.9, 
then it would roll over to 4.

### EOF ###
