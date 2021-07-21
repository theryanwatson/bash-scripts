### [alldirs](alldirs)
Will perform any task over all directories in the current directory, non-recursively.

###### Usage:
* `alldirs git branch`
* `alldirs ls -l`
* `alldirs rm *.bak`

### [delete-nexus-artifacts](delete-nexus-artifacts)
Deletes the various maven artifacts associated with jars, poms, javadoc, etc

###### Usage:
* `delete-nexus-artifacts {{ path-to-directory }} {{ app-name }} {{ major-minor-version }} {{ starting-patch-version-inclusive }} {{ ending-patch-version-exclusive }}`
  * `delete-nexus-artifacts "https://nexus.my-company.com/repository/maven-releases/com/my-company/" "my-app" "1.0" 14 65`

### [idea](idea)
Opens the current folder in Idea IntelliJ.

###### Usage:
* `cd {{ project folder}}; idea`
  * `cd /site/my-project; idea`

### [update-projects](update-projects)
Loops over all project directories and does a `git pull; git fetch --tags`. Assumes projects are all in `~/projects/`. Add any additional project folders to the bottom, like `cd ~/my-stuff; updateDirs`
