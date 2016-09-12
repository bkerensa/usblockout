# Session USB Lockout

This program provides a way to toggle Grsecurity Deny New USB feature with the state of a user session.
That is, it will automatically enable the feature when the screen is locked or the session exists, and vice versa.

## Caveats

**Beware!** If you use some sort of USB device (ex: a yubikey) for pam logins, login will be entierly broken!

## Building

Provided in this repository is a debian branch which is used to build a deb package from git tags:

	git checkout -b debian https://github.com/subgraph/usblockout.git
	cd usblockout
	gbp buildpackage -us -uc
	dpkg -i /tmp/subgraph-usblockout_#VERSION#.deb