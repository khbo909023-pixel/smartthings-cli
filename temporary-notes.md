Collected notes to eventually include in the yargs release notes.

* All commands now have examples in their help (`smartthings <command> --help`).
* args that require enum-like types are now case-insensitive. e.g. You can now list zigbee devices
  with `smartthings devices --type zigbee`.
* The config file location is now determined by https://www.npmjs.com/package/env-paths[envPaths] library
  rather than oclif. A reasonable attempt has been made at finding the old config and copying it for
  the user so normally no change is needed other than making changes in the new file if necessary.
  The `config` command now displays the name of the configuration file.
* Commands that take a capability specification on the command line now get the version from a flag
  rather than an argument. e.g. `smartthings capabilities myteam.myCapability --capability-version 1`
  instead of `smartthings capabilities myteam.myCapability 1`
* We now ES modules.
* We have migrated to yargs, replacing oclif.
