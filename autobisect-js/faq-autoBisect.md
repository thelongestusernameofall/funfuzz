## FAQ

Q: Compilation is broken! How do I use autoBisect to see when the builds broke?

...

Q: Compilation has finished breaking. How do I know when the builds were working again?

...

Q: What should I do with the known broken changeset ranges to prevent autoBisect from retesting those revisions?

...

Q: The testcase is giving out assorted varied exit codes as it gets executed by older binaries. How can I fixate to a particular interesting exit code?

...

Q: The testcase is intermittent and giving weird results! What should I do to try and get more reliable results?

...

Q: What happens when a new operating system is released, and we now have a new changeset hash that has to be updated as the earliest known working revision?

...

Q: Does autoBisect work on nightly SpiderMonkey js shells yet?

No, not yet. Currently it only uses ["tinderbox-builds" js shells](https://ftp.mozilla.org/pub/mozilla.org/firefox/tinderbox-builds/mozilla-inbound-macosx64-debug/) by default, which are stored on a per-checkin basis only for the past month. Patches accepted!

Q: How does autoBisect compare with [mozregression](http://mozilla.github.io/mozregression/)?

When autoBisect was proposed and written in 2009, mozregression did not exist yet. Since 2010, both have been developed independently of each other.

autoBisect was [first written](https://bugzilla.mozilla.org/show_bug.cgi?id=482536) (in Bash) [with results](https://bugzilla.mozilla.org/show_bug.cgi?id=476655#c8) in March 2009.

mozregression had its [first landing](https://github.com/mozilla/mozregression/commit/d50509b36cb6ba45d7c54917f528bdf482d2c5e6) in February 2010.

autoBisect supports bisections using compiled and downloaded (tinderbox-builds) SpiderMonkey js shells (with rudimentary support for Firefox), while mozregression supports nightly and inbound builds [for various Mozilla products](http://mozilla.github.io/mozregression/).