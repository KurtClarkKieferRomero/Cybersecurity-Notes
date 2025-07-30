2025-07-13 00:14

Status: **Incomplete**

Tags: 
[[Kali Linux]]
[[Basics]]
[[Update cmds]]
[[git]]
## Install and Update Tools

`apt-get update && apt-get upgrade` which means "Get the information about the packages and check if it matches AND if there is a newer package or version about that, install it."  This is meant to update the library or package information about a program or tool and update (upgrade lol) them to the latest version if possible. The output will be:
	`The following packages are no longer required:`
		`packages here....`
	`The following packages will be upgraded:`
		`packages here....`
If you want to install packages use the command `apt-get install packageName` for example
	`apt-get install git`

**git**
	Related to *github* which houses many different tools that are not installed in kali. This is important to know because you can find many different tools that are not primarily installed in kali

**Note**: This can be used to install files or packages inside the infected host but of course it needs to be quiet or does not show any cmd's. You also should have elevated authority to perform this action. Also here is the [man](https://linux.die.net/man/8/apt-get) page for `apt-get` It mention the use of -q which means quiet and will not show any progress, using -qq will make it more hidden in a sense.
### Reference
