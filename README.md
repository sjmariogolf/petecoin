# petecoin
The Official Download Source for PeteCoin aka petecoin
# Petecoin Core [PETE, P]
==========================

![Petecoin] (http://i60.tinypic.com/2i9t5kw.jpg)

## Back Yard Talk
### {Bob}   --  Wow! This looks JUST like that other coin...You know...
![Bob] (http://i58.tinypic.com/1239phw.jpg)
### {Petey} -- No Shibe! I found ONE "mining" in my back yard.
![Petey] (http://i60.tinypic.com/30907s2.jpg)
### {Petey} -- These shiny things are totally tasteless. You'd be wasting your time, not to mention your toenails digging ANY of these up from this WORTHLESS hard ground!

## What is Petecoin?
Petecoin is a cryptocurrency like Bitcoin, although it does not use SHA256 as its proof of work (POW). Taking development cues from "Dogecoin" (...a great coin worthy of such praise, much kindness, providing many real opportuinity to learn, and a wonderful coin (wow!) from which to derive...), Petecoin currently employs a simplified variant of scrypt.    

### How much doge can exist?
Same as the predecessors'.

### How many bones (I mean conis) will I find?
A different payout scheme was envisioned with block rewards being determined by taking the maximum reward as per the block schedule and applying the result of a Mersenne Twister pseudo-random number generator to arrive at a number between 1 and the maximum reward for that block transition.

##Scheme
###The current block reward schedule:
Halving =  500,000 blocks
Blocks
 -       <> 10,000 (1-999)
 -       <> 20,000 (1-1999)
 -       <> 30,000 (1-2999)
 -       <> 40,000 (1-3999)
 -       <> 50,000 (1-4999)
 -       <> 60,000 (1-5999)
 -       <> 70,000 (1-6999)
 -       <> 80,000 (1-7999)
 -       <> 90,000 (1-8999)
 -       else      (9999)

## Algo
Simplified scrypt
./minerd  -a scrypt -o stratum+tcp://199.99.99.99:9999 -O petethedog.pete:bone

### Ports
RPC 22666
P2P 22665

## Mining
Beg!

## Exchanges
Whine! Whimper! Bark!

## Wallets
![Windows] Windows (http://i59.tinypic.com/2jfggsn.jpg)
Available upon launch

![Linux] Daemon, and Wallet (http://i62.tinypic.com/kdvnyp.jpg)
Available upon launch






### make petecoind/petecoin-cli/petecoin-qt

  The following are developer notes on how to build Petecoin on your native platform. They are not complete guides, but include notes on the necessary libraries, compile flags, etc.

  - [OSX Build Notes](doc/build-osx.md)
  - [Unix Build Notes](doc/build-unix.md)
  - [Windows Build Notes](doc/build-msw.md)

Translations
------------

Changes to translations as well as new translations can be submitted to
[Bitcoin Core's Transifex page](https://www.transifex.com/projects/p/bitcoin/).

Periodically the translations are pulled from Transifex and merged into the git repository. See the
[translation process](doc/translation_process.md) for details on how this works.

If the changes are Petecoin specific, they can be submitted as pull request against this repository.
If it is a general translation, consider submitting it through upstream, as we will pull these changes later on.

Development tips and tricks
---------------------------

**compiling for debugging**

Run configure with the --enable-debug option, then make. Or run configure with
CXXFLAGS="-g -ggdb -O0" or whatever debug flags you need.

**debug.log**

If the code is behaving strangely, take a look in the debug.log file in the data directory;
error and debugging message are written there.

The -debug=... command-line option controls debugging; running with just -debug will turn
on all categories (and give you a very large debug.log file).

The Qt code routes qDebug() output to debug.log under category "qt": run with -debug=qt
to see it.

**testnet and regtest modes**

Run with the -testnet option to run with "play petecoins" on the test network, if you
are testing multi-machine code that needs to operate across the internet.

If you are testing something that can run on one machine, run with the -regtest option.
In regression test mode blocks can be created on-demand; see qa/rpc-tests/ for tests
that run in -regest mode.

**DEBUG_LOCKORDER**

Petecoin Core is a multithreaded application, and deadlocks or other multithreading bugs
can be very difficult to track down. Compiling with -DDEBUG_LOCKORDER (configure
CXXFLAGS="-DDEBUG_LOCKORDER -g") inserts run-time checks to keep track of what locks
are held, and adds warning to the debug.log file if inconsistencies are detected.

