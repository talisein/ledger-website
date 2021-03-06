# On Reconciling

I use emacs to edit and reconcile my corporate ledger.

First, I download my bank transactions (from Bank of America) and \
use a [trivial python
script](http://sixthdev.versionhost.com/viewvc.cgi/ledger/bofaconvert.py?view=markup)\
to convert them to ledger format.

I open two emacs windows (M-x new-frame) so I can edit the \
bank statement and my ledger side by side.

This is a great setup even if you just want to use ledger-reconcile.
However, \
I’m particularly picky about keeping the effective dates filled in, so
as I work \
through the bank statement, I just update my ledger by hand, and mark
each\
entry as cleared (with a \* ) as I go.

To check my work, I keep a terminal window open that constantly monitors
the \
cleared balance:

     watch ledger --cleared bal asset:checking

This constant feedback seems to prevent data entry errors on my part,
and\
the two-window mode lets me move fairly quickly.

Converting the bank data to ledger format turns out to be MUCH nicer
than\
using a paper statement or even working directly from online banking,
because\
if you’re missing a transaction, you can just cut and paste.

-MichalWallace

* * * * *

I’ve got a [similar (Haskell)
script](http://www.khjk.org/log/2009/oct/ledger.html) for CSV-data,
along with some tips on fetching the data via HBCI (online API provided
by most German banks):

-Pesco
