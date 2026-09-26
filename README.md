RetroPie-Setup
==============

What's different in this fork
-----------------------------

This repository (`grioghar/retropie-redux`) is a fork of
[RetroPie/RetroPie-Setup](https://github.com/RetroPie/RetroPie-Setup).

**As of 2026-09-26 it carries no changes of its own.** The fork's `master`
branch is identical to upstream `master` at commit
[`15e11ce3`](https://github.com/RetroPie/RetroPie-Setup/commit/15e11ce388f5c4b9ffe4a5f300f071ff63cbdbd5)
("openmsx: clear scriptmodule file exec bit", 2026-05-23): zero unique
commits, and `git diff upstream/master...master` is empty. Upstream has moved
on since then — its `master` is 40 commits ahead (at
[`664d2537`](https://github.com/RetroPie/RetroPie-Setup/commit/664d2537d310edea267994097f800f82387f1a5d),
"skyscraper: updates to scriptmodule (#4229)", 2026-09-16), so this fork is
currently *behind* upstream rather than ahead of it.

`master` is the only branch in this fork; there are no divergent feature
branches holding unmerged work. The only fork-specific content is this
section itself, added on the `chore/repo-hygiene-2026-09` branch.

<!-- PLACEHOLDER(greg): what is "redux" meant to become? Once the fork diverges, replace the paragraph above with a summary of the changes grouped by theme, plus the commit count and the upstream commit they were compared against. -->

To bring the fork level with upstream:

```shell
git remote add upstream https://github.com/RetroPie/RetroPie-Setup.git
git fetch upstream master
git merge --ff-only upstream/master
```

General Usage
-------------

Shell script to setup the Raspberry Pi, Vero4K, ODroid-C1 or a PC running Ubuntu with many emulators and games, using EmulationStation as the graphical front end. Bootable pre-made images for the Raspberry Pi are available for those that want a ready-to-go system, downloadable from the releases section of GitHub or via our website at https://retropie.org.uk.

This script is designed for use on Raspberry Pi OS (previously called Raspbian) on the Raspberry Pi, OSMC on the Vero4K or Ubuntu on the ODroid-C1 or a PC.

To run the RetroPie Setup Script make sure that your APT repositories are up-to-date and that Git is installed:

```shell
sudo apt-get update
sudo apt-get dist-upgrade
sudo apt-get install git
```

Then you can download the latest RetroPie setup script with:

```shell
cd
git clone --depth=1 https://github.com/RetroPie/RetroPie-Setup.git
```

The script is executed with:

```shell
cd RetroPie-Setup
sudo ./retropie_setup.sh
```

When you first run the script it may install some additional packages that are needed.

Binaries and Sources
--------------------

On the Raspberry Pi, RetroPie Setup offers the possibility to install from binaries or source. For other supported platforms only a source install is available. Installing from binary is recommended on a Raspberry Pi as building everything from source can take a long time.

For more information, visit the site at https://retropie.org.uk or the repository at https://github.com/RetroPie/RetroPie-Setup.

Docs
----

You can find useful information about several components and answers to frequently asked questions in the [RetroPie Docs](https://retropie.org.uk/docs/). If you think that there is something missing, you are invited to submit a pull request to the [RetroPie-Docs repository](https://github.com/RetroPie/RetroPie-Docs).


Thanks
------

This script just simplifies the usage of the great works of many other people that enjoy the spirit of retrogaming. Many thanks go to them!
