node {
    stage('Clone sources') {
        git url: 'https://github.com/jayyousi/jenkins_training.git'
    }
    
    stage('Maven build') {
        def mvnHome = tool 'Training'
        sh "${mvnHome}/bin/mvn clean install -DskipTests"
    }
}
