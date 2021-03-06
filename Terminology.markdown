# Terminology

Ledger doesn’t really enforce any kind of accounting principles, so
you’re free to name things however you like. In essence, Ledger’s just a
fancy calculator for moving quantities of “stuff” between “accounts”.
Even those definitions are flexible, however, which makes for some
interesting possible use cases.

In the accounting case, however, there are some terms that I use
throughout the source code that may make some of the docs easier to
understand. Here they are:

### Journal

Any file that contains Ledger data is called a “journal”. A journal
mostly contains “transactions”, but it can also contain control
directives, comments, and a few other things.

### Transaction

A transaction represents something that you want to enter into your
journal. For example, if you just cashed a paycheck from your employer
by depositing it into your bank account, this entire action is called an
“transaction”. The total cost of every transaction must balance to zero,
otherwise Ledger will refuse to read your journal file any further. This
guarantee that no amounts can be lost due to balancing errors.

### Posting

Each transaction is made up of two or more postings (there is a special
case that allows for just one, using virtual postings).

### Account

An account is any place that accumulates quantities, of any meaning.
They can be named anything, the names can even contain spaces, and they
can mean whatever you want. Students of accounting will use five
top-level names: Equity, Assets, Liabilities, Expenses, Income. All
other accounts are specified as children of these accounts. This is not
required by Ledger, however, nor does it even know anything about what
these names mean. That’s all left up to the user.
