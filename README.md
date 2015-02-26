

    * git pull --rebase - use this for good commit history

# release and deploy new version
## mvn release:prepare -Prelease 
    * creates new version
    * adds tag by version in branch
    * pushes to remote repository with tag
## mvn release:perform -Prelease
    * creates new SNAPSHOT version
    * builds <module-name>-x.x.x.jar, <module-name>-x.x.x-sources.jar, <module-name>-x.x.x-javadoc.jar
    * and uploads on nexus repository
