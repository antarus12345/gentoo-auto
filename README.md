Auto-Gentoo
===========

Auto Gentoo consists of a few ideas; some already implemented and others in their infancy.

The goals of Auto Gentoo are:

 - Reduce developer toil.
 - Reduce defects exposed to users.
 - Increase velocity of packages becoming available to users.
 - Increase velocity of packages being marked 'stable'.

## Defects ##

Currently users of Gentoo consume Gentoo in two typical ways:

1. Users consume an rsync mirror of the Gentoo Repo; the mirror tends to be 30-60 minutes behind master (due to various syncs mirroring delay.)
  There is no QA between contributors merging changes into the master branch and the changes being mirrored to users.
1. Users consume a git mirror of Gentoo. Typically they consume the main Gentoo repo git mirror. This mirror has no specific delays.
  There is no QA between contributors merging changes into the master branch and users pulling the changes down.

Auto Gentoo considers a third approach, where some automated (but never manual) QA jobs are run between commits to the master branch
and the commits being published to end users. The tests are explicitly not intended to catch all errors (and this is a non-goal of
Auto Gentoo). However Auto Gentoo believes that with a reasonable suite, many defects can be resolved prior to being observed by
end users.

This is currently implemented in https://github.com/gentoo-mirror/gentoo.

One potential concern of this approach is that now we end up with two repositories:

1. ::gentoo (master)
1. ::gentoo (qa)

There should be some objective that qa does not lag behind (e.g. that issues in the master branch that cause QA tests to fail are resolved in a reasonable timeframe. We are currently unsure what the objectives should be, but will collect data to determine what is feasible (given staffing) and what users are willing to tolerate.

## Velocity ##

These efforts aim to replace manual work by developers. They are not particularly thought out at the moment.

### Auto Bumper ###
### Auto Stabler ###
