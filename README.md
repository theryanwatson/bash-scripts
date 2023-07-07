## Download and chmod scripts:
```bash
mkdir -p ~/bin; for s in alldirs fix-newlines idea update-projects; do wget https://raw.githubusercontent.com/theryanwatson/bash-scripts/main/${s} -O ~/bin/${s}; chmod +x ~/bin/${s}; done
```

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

### [fix-newlines](fix-newlines)
When a file has Windows newlines

###### Usage:
* `fix-newlines {{ file-to-fix }}`
  * `fix-newlines ./gradlew`

### [idea](idea)
Opens the current folder in Idea IntelliJ. WSL version assumes `idea64.exe` is in path.

###### Usage:
* `cd {{ project folder}}; idea`
  * `cd /site/my-project; idea`

### [update-projects](update-projects)
Loops over all project directories and does a `git pull; git fetch --tags`. Assumes projects are all in `~/projects/`. Add any additional project folders to the bottom, like `cd ~/my-stuff; updateDirs`
