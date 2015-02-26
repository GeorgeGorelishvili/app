

    * git pull --rebase - use this for good commit history

## project build
     * mvn clean install (package)         - builds modules: eflow-core, eflow-patch, eflow-reports
     * mvn clean install (package) -Peflow - builds modules: eflow-core, eflow-patch, eflow-reports, eflow-web
     * mvn clean install (pachage) -Pmia   - builds modules: eflow-core, eflow-patch, eflow-reports, persons, protocols, eflow-services, eflow-jobs, interflow-jobs, eflow-ear


# release and deploy new version
## mvn release:prepare -Prelease 
    * creates new version
    * adds tag by version in branch
    * pushes to remote repository with tag
## mvn release:perform -Prelease
    * creates new SNAPSHOT version
    * builds <module-name>-x.x.x.jar, <module-name>-x.x.x-sources.jar, <module-name>-x.x.x-javadoc.jar
    * and uploads on nexus repository
