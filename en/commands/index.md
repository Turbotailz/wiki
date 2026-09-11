---
title: Command usage
description: Overview of LuckPerms commands.
---

Command usage is printed to the console/chat whenever invalid arguments are provided. **Simply typing /lp** will list all commands a user has permission to use.

If the only thing returned when you type a command is the plugin version, you do not have permission to use any of the commands. You need to use the server console to [give yourself access to LuckPerms commands first](/wiki/getting-started#granting-full-access-to-modify-permissions).

## Aliases
A list of aliases for each platform are listed below. Each command works in exactly the same manner, so you can use whichever you prefer.

| Bukkit / Sponge / Fabric / Forge / Nukkit   | BungeeCord         | Velocity             |
| ----------------------------------- | ------------------ | -------------------- |
| `/lp`                               | `/lpb`             | `/lpv`               |
| `/luckperms`                        | `/luckpermsbungee` | `/luckpermsvelocity` |
| `/permissions` (*deprecated*)       |                    |                      |
| `/perms` (*deprecated*)             |                    |                      |
| `/perm` (*deprecated*)              |                    |                      |

**`Important:`** The command aliases are different on BungeeCord and Velocity. This is so you can choose where the command is executed. If the aliases were the same, you would never be able to control LuckPerms on a backend server as the command would always be handled by the proxy!

If you are using Bukkit/Spigot, by default, all users with OP have access to LuckPerms commands. You can change this in the config.

## Overview
### Arguments Key:
* `<required>` - you *must* specify this argument when running the command
* `[optional]` - you do not need to specify this argument. a default will be used if not given.

If you want to include spaces in arguments, you must escape the argument with quotes. `"  "`

The alias used below (`/lp`) can be exchanged for any of the ones listed in the aliases section above.

### General commands
General commands used to operate LuckPerms functions.

*  [/lp](/wiki/commands/general#lp)
*  [/lp `sync`](/wiki/commands/general#lp-sync)
*  [/lp `info`](/wiki/commands/general#lp-info)
*  [/lp `editor`](/wiki/commands/general#lp-editor-type)
*  [/lp `verbose` \<on | record | off | upload\> [filter]](General-Commands#lp-verbose-onrecordoffupload-filter)
*  [/lp `tree` [scope] [player]](General-Commands#lp-tree-scope-player)
*  [/lp `search` [comparison] \<permission\>](General-Commands#lp-search-comparison-permission)
*  [/lp `networksync`](/wiki/commands/general#lp-networksync)
*  [/lp `import` \<file | code --upload\> [--replace]](General-Commands#lp-import-filecode---upload---replace)
*  [/lp `export` \<file\> [--upload]](General-Commands#lp-export-file--upload)
*  [/lp `reloadconfig`](/wiki/commands/general#lp-reloadconfig)
*  [/lp `bulkupdate`](/wiki/commands/general#lp-bulkupdate-data-type-action-action-field-action-value-constraints)
*  [/lp `translations`](/wiki/commands/general#lp-translations)
*  [/lp `creategroup` \<group\> [weight] [displayname]](General-Commands#lp-creategroup-name-weight-displayname)
*  [/lp `deletegroup` \<group\>](/wiki/commands/general#lp-deletegroup-name)
*  [/lp `listgroups`](/wiki/commands/general#lp-listgroups)
*  [/lp `createtrack` \<track\>](/wiki/commands/general#lp-createtrack-name)
*  [/lp `deletetrack` \<track\>](/wiki/commands/general#lp-deletetrack-name)
*  [/lp `listtracks`](/wiki/commands/general#lp-listtracks)

### User commands
Commands used to view or modify a specific user.

Formed of `/lp user <user> ...` - where `<user>` is the username or uuid of the user being queried / modified.
*  [/lp user \<user\> `info`](/wiki/commands/user#lp-user-user-info)
*  [/lp user \<user\> `permission`](/wiki/commands/permission)
*  [/lp user \<user\> `parent`](/wiki/commands/parent)
*  [/lp user \<user\> `meta`](/wiki/commands/meta)
*  [/lp user \<user\> `editor`](/wiki/commands/user#lp-user-user-editor)
*  [/lp user \<user\> `promote` \<track\> [context...]](User-Commands#lp-user-user-promote-track-context)
*  [/lp user \<user\> `demote` \<track\> [context...]](User-Commands#lp-user-user-demote-track-context)
*  [/lp user \<user\> `showtracks`](/wiki/commands/user#lp-user-user-showtracks)
*  [/lp user \<user\> `clear` [context...]](User-Commands#lp-user-user-clear-context)
*  [/lp user \<user\> `clone` \<user\>](/wiki/commands/user#lp-user-user-clone-user)

### Group commands
Commands used to view or modify a specific group.

Formed of `/lp group <group> ...` - where `<group>` is the name of the group being queried / modified.
*  [/lp group \<group\> `info`](/wiki/commands/group#lp-group-group-info)
*  [/lp group \<group\> `permission`](/wiki/commands/permission)
*  [/lp group \<group\> `parent`](/wiki/commands/parent)
*  [/lp group \<group\> `meta`](/wiki/commands/meta)
*  [/lp group \<group\> `editor`](/wiki/commands/group#lp-group-group-editor)
*  [/lp group \<group\> `listmembers` [page]](Group-Commands#lp-group-group-listmembers-page)
*  [/lp group \<group\> `setweight` \<weight\>](/wiki/commands/group#lp-group-group-setweight-weight)
*  [/lp group \<group\> `setdisplayname` \<name\>](/wiki/commands/group#lp-group-group-setdisplayname-name)
*  [/lp group \<group\> `showtracks`](/wiki/commands/group#lp-group-group-showtracks)
*  [/lp group \<group\> `clear` [context...]](Group-Commands#lp-group-group-clear-context)
*  [/lp group \<group\> `rename` \<new name\>](/wiki/commands/group#lp-group-group-rename-new-name)
*  [/lp group \<group\> `clone` \<name of clone\>](/wiki/commands/group#lp-group-group-clone-new-name)

### Permission commands
Commands used to view or modify the permissions data of a specific user or group.

Formed of either `/lp user <user> permission ...` or `/lp group <group> permission ...`
*  [`info`](/wiki/commands/permission#lp-usergroup-usergroup-permission-info)
*  [`set` \<node\> \<true/false\> [context...]](Permission-Commands#lp-usergroup-usergroup-permission-set-node-truefalse-context)
*  [`unset` \<node\> [context...]](Permission-Commands#lp-usergroup-usergroup-permission-unset-node-context)
*  [`settemp` \<node\> \<true/false\> \<duration\> [temporary modifier] [context...]](Permission-Commands#lp-usergroup-usergroup-permission-settemp-node-truefalse-duration-temporary-modifier-context)
*  [`unsettemp` \<node\> [duration] [context...]](Permission-Commands#lp-usergroup-usergroup-permission-unsettemp-node-duration-context)
*  [`check` \<node\>](/wiki/commands/permission#lp-usergroup-usergroup-permission-check-node)
*  [`clear` [context...]](Permission-Commands#lp-usergroup-usergroup-permission-clear-context)

### Parent commands
Commands used to view or modify the inheritance properties (parents) of a specific user or group.

Formed of either `/lp user <user> parent ...` or `/lp group <group> parent ...`
*  [`info`](/wiki/commands/parent#lp-usergroup-usergroup-parent-info)
*  [`set` \<group\> [context...]](Parent-Commands#lp-usergroup-usergroup-parent-set-group-context)
*  [`add` \<group\> [context...]](Parent-Commands#lp-usergroup-usergroup-parent-add-group-context)
*  [`remove` \<group\> [context...]](Parent-Commands#lp-usergroup-usergroup-parent-remove-group-context)
*  [`settrack` \<track\> \<group\> [context...]](Parent-Commands#lp-usergroup-usergroup-parent-settrack-track-group-context)
*  [`addtemp` \<group\> \<duration\> [temporary modifier] [context...]](Parent-Commands#lp-usergroup-usergroup-parent-addtemp-group-duration-temporary-modifier-context)
*  [`removetemp` \<group\> [duration] [context...]](Parent-Commands#lp-usergroup-usergroup-parent-removetemp-group-duration-context)
*  [`clear` [context...]](Parent-Commands#lp-usergroup-usergroup-parent-clear-context)
*  [`cleartrack` \<track\> [context...]](Parent-Commands#lp-usergroup-usergroup-parent-cleartrack-track-context)
*  [`switchprimarygroup` \<group\>](/wiki/commands/parent#lp-user-user-parent-switchprimarygroup-group)

### Meta commands
Commands used to view or modify the metadata of a specific user or group.

Formed of either `/lp user <user> meta ...` or `/lp group <group> meta ...`
*  [`info`](/wiki/commands/meta#lp-usergroup-usergroup-meta-info)
*  [`set` \<key\> \<value\> [context...]](Meta-Commands#lp-usergroup-usergroup-meta-set-key-value-context)
*  [`unset` \<key\> [context...]](Meta-Commands#lp-usergroup-usergroup-meta-unset-key-value-context)
*  [`settemp` \<key\> \<value\> \<duration\> [temporary modifier] [context...]](Meta-Commands#lp-usergroup-usergroup-meta-settemp-key-value-duration-temporary-modifier-context)
*  [`unsettemp` \<key\> [context...]](Meta-Commands#lp-usergroup-usergroup-meta-unsettemp-key-context)
*  [`addprefix` \<priority\> \<prefix\> [context...]](Meta-Commands#lp-usergroup-usergroup-meta-addprefix-priority-prefix-context)
*  [`addsuffix` \<priority\> \<suffix\> [context...]](Meta-Commands#lp-usergroup-usergroup-meta-addsuffix-priority-suffix-context)
*  [`setprefix` [priority] \<prefix\> [context...]](Meta-Commands#lp-usergroup-usergroup-meta-setprefix-priority-prefix-context)
*  [`setsuffix` [priority] \<suffix\> [context...]](Meta-Commands#lp-usergroup-usergroup-meta-setsuffix-priority-suffix-context)
*  [`removeprefix` \<priority\> [prefix] [context...]](Meta-Commands#lp-usergroup-usergroup-meta-removeprefix-priority-prefix-context)
*  [`removesuffix` \<priority\> [suffix] [context...]](Meta-Commands#lp-usergroup-usergroup-meta-removesuffix-priority-suffix-context)
*  [`addtempprefix` \<priority\> \<prefix\> \<duration\> [temporary modifier] [context...]](Meta-Commands#lp-usergroup-usergroup-meta-addtempprefix-priority-prefix-duration-temporary-modifier-context)
*  [`addtempsuffix` \<priority\> \<suffix\> \<duration\> [temporary modifier] [context...]](Meta-Commands#lp-usergroup-usergroup-meta-addtempsuffix-priority-suffix-duration-temporary-modifier-context)
*  [`settempprefix` [priority] \<prefix\> \<duration\> [temporary modifier] [context...]](Meta-Commands#lp-usergroup-usergroup-meta-settempprefix-priority-prefix-duration-temporary-modifier-context)
*  [`settempsuffix` [priority] \<suffix\> \<duration\> [temporary modifier] [context...]](Meta-Commands#lp-usergroup-usergroup-meta-settempsuffix-priority-suffix-duration-temporary-modifier-context)
*  [`removetempprefix` \<priority\> [prefix] [context...]](Meta-Commands#lp-usergroup-usergroup-meta-removetempprefix-priority-prefix-context)
*  [`removetempsuffix` \<priority\> [suffix] [context...]](Meta-Commands#lp-usergroup-usergroup-meta-removetempsuffix-priority-suffix-context)
*  [`clear` [context...]](Meta-Commands#lp-usergroup-usergroup-meta-clear-context)

### Track commands
Commands used to view or modify a specific track.

Formed of `/lp track <track> ...` - where `<track>` is the name of the track being queried / modified.
*  [/lp track \<track\> `info`](/wiki/commands/track#lp-track-track-info)
*  [/lp track \<track\> `editor`](/wiki/commands/track#lp-track-track-editor)
*  [/lp track \<track\> `append` \<group\>](/wiki/commands/track#lp-track-track-append-group)
*  [/lp track \<track\> `insert` \<group\> \<position\>](/wiki/commands/track#lp-track-track-insert-group-position)
*  [/lp track \<track\> `remove` \<group\>](/wiki/commands/track#lp-track-track-remove-group)
*  [/lp track \<track\> `clear`](/wiki/commands/track#lp-track-track-clear)
*  [/lp track \<track\> `rename` \<new name\>](/wiki/commands/track#lp-track-track-rename-new-name)
*  [/lp track \<track\> `clone` \<name of clone\>](/wiki/commands/track#lp-track-track-clone-new-name)

### Log commands
Commands used to view the action log.
*  [/lp log `recent` [user] [page]](Log-Commands#lp-log-recent-user-page)
*  [/lp log `search` \<query\> [page]](Log-Commands#lp-log-search-query-page)
*  [/lp log `notify` [on|off]](Log-Commands#lp-log-notify-onoff)
*  [/lp log `userhistory` \<user\> [page]](Log-Commands#lp-log-userhistory-user-page)
*  [/lp log `grouphistory` \<group\> [page]](Log-Commands#lp-log-grouphistory-group-page)
*  [/lp log `trackhistory` \<track\> [page]](Log-Commands#lp-log-trackhistory-track-page)
