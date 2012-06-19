__This script is of 2006. It's a old script but you can use it for your migration project and update it ([pull request](https://github.com/llaumgui/xoops2punbb/pull/new/master) or [code review](https://projects.llaumgui.com/p/xoops2punbb/review/)).__

It converts from a [Xoops 2.0](http://www.xoops.org/) board (CBB or newBB) to a [PunBB](http://punbb.informer.com/) 1.0.

Prerequisites
=============
* PHP4 or higher.
* php-cli to start the script from the command line. I have not tested with a browser but it should work anyway.
* Some knowledge of php.

This script converts
===================
* Groups of members: The permissions will be the same for all groups. They will therefore change later.
* Members:
 * Xoops allowing multiple groups to a single member, that punBB do not, the members are all tarred with the same group members (id = 4).
 * Another small subtlety punBB, the member ID 1 is the guest, we must not have a member with uid = 1 under Xoops. If this is your case, you will have a small mill by modifying my script.
 * Avatars must put them all in the correct folders (img / avatars).
* Categories.
* Forums.
* Topics
* Posts: It is the big piece, there is a batch processing for large databases.
