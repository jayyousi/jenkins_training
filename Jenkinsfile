node {
    // Get Artifactory server instance, defined in the Artifactory Plugin administration page.
    def server = Artifactory.server "jfrog"
    // Create an Artifactory Maven instance.
    def rtMaven = Artifactory.newMavenBuild()
    def buildInfo

    stage('Clone sources') {
        git url: 'https://github.com/jayyousi/jenkins_training.git'
    }
    
    stage('Maven build') {
        def mvnHome = tool 'maven-3'
        sh "${mvnHome}/bin/mvn clean install -DskipTests"
    }
}
