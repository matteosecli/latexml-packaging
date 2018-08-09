

Maintaining notes (for myself)
====================

Changelog file
--------------
For a new version, you have to manually update the `changelog` file. Open up a terminal in the `debian` directory (or even in the parent folder) and type (for, e.g., release 0.8.2-1)

    $ export DEBFULLNAME='Matteo Seclì'
    $ export DEBEMAIL='secli.matteo@gmail.com'
    $ dch --newversion 0.8.2-1 --check-dirname-level 0 --controlmaint 'New upstream release (0.8.2-1)'
    $ dch --release --distribution unstable --check-dirname-level 0 ''

Then, update the repo and let Launchpad work its magic.

Warnings
--------
* ~~Dunno why, but my email is not parsed correctly. I have to figure out what's the problem.~~ An `export` was necessary.
* ~~The goddamn Launchpad does not accept signed commits, so I had to switch back to unsigned commits.~~ Not really solved, but now I'm using git-to-git imports in Launchpad to bypass this problem.
