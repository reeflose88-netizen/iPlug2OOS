# CLAUDE.md

## iPlug2OOS "out of source"

This repository is based off of the [iPlug2OOS "out of source" repo](https://github.com/iPlug2/iPlug2OOS.git). It contains the iPlug2 framework as a git submodule in the @iPlug2 folder and template plugin project code in @TemplateProject.

@TemplateProject can be duplicated using @duplicate.py at the top level of the repo in order to create a new iPlug2 project with a unique name. If there is no other folder existing already we can assume this is a fresh clone, otherwise we may want to pick up and carry on with a previously cloned project. Typically @TemplateProject can remain in order that more projects may be added to the repo via duplication at a later stage.

### Cloning TemplateProject

```bash
./duplicate.py TemplateProject [outputprojectname] [manufacturername]
```

outputprojectname and manufacturername are mandatory and should not contain spaces e.g.

```bash
./duplicate.py TemplateProject MyNewAudioPlugin MyBrandName
```

once the template has been cloned, ask the user if they want to commit the newly cloned project and modified top level config files using the following commands...

```bash
git add MyNewAudioPlugin/* # the newly cloned plugin project
git add .vscode/* # vscode launch.json and tasks.json for the top level iPlug2OOS.code-workspace file
git add .github/* # github actions
git add bump_version.py # a script that can be used to bump the version number in  
git commit -m "created MyNewAudioPlugin based on TemplateProject"
```

### Building the cloned project

The structure of an iPlug2 project is described in @iPlug2/Documentation/structure.md

## Additional instructions
- iPlug2 @iPlug2/Documentation/CLAUDE.md
