# Changelog

## 1.10.2
Disabled **Close Current** since it currently breaks in Atom. Will enable it again as soon as there is a good solution to fix it.

## 1.10.1
Bugfix

## 1.10.0
- You can now add a `group:` setting on a project and sort the projects list by group.
- Added a marker for projects with `devMode: true` to the projects list to make it more clear that it will open in developer mode

## 1.9.3
Did a fix that might fix an error that sometimes came up when updating to latest version.
If an error still comes up, try updating to latest version of Atom, currently 0.135

## 1.9.2
Bug fix

## 1.9.1
Now using the updated config system. If you were using "sort by title" you will have to set it again with the new sort by option.

## 1.9.0
- You can now add templates in the projects file.

## 1.8.2
Now using FS instead of pathwatcher for monitoring changes in the projects file.

## 1.8.1
- **Project Manager: Edit Projects** will now open file in the current window instead of a new one
- Added possibility to open project in dev mode with `devMode: true`

## 1.8.0
Changed the way settings work which mean that if you have used any of the old settings, you have to redo them. This way all settings that can be set from the settings view/config.cson can be project specific.

```CoffeeScript
# Old way
'settings':
  'setTabLength': 2

# New way
'settings':
  'editor.tabLength': 2
  'editor.showIndentGuide': true
  'project-manager.showPath': true
```

## 1.7.6
Miss read the updated Atom::open() API so going back to the old way of closing
the current window, but with a fix to it.

## 1.7.5
Now use the updated Atom::open() API

## 1.7.4
- Removed Project Manager from the context menu since it has nothing todo with the interface.
- Some code cleanup and fix

## 1.7.3
- Fixed inconsistency in filename in README and CHANGELOG.
- Added brackets around hostname in `projects.[hostname].cson` to make it clearer that that part will change to use the hostname of the environment.

## 1.7.2
- Updated changelog

## 1.7.1
- Updated readme

## 1.7
*Something seems to have happend during publish so 1.6 was skipped*
- Project path now shows when saving a project

## 1.5
This update adds an option for **environment specific project** files which are based on your hostname to be able to sync the atom folder between environments without ignoring `projects.cson`.
Enabling this option will create a `projects.[hostname].cson` file.

After enabling this option you will have to manually move the contents of `projects.cson` to the new `projects.[hostname].cson` file. After this `projects.cson`can be delete or left alone.

## 1.4
- Added option to sort by title.
- Added changelog