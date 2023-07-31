
pipeline {
    agent any

    stages {
      

        stage('Build with Maven') {
            steps {
                script {
                    // Run Maven build
                    sh 'mvn clean package -DskipTests=true'

                    // Save artifacts (JAR files) to the workspace for later use
                    // Adjust the path based on your project's output directory
                    sh 'cp target/*.jar $WORKSPACE/'
                }
            }
        }

        // Add other stages as needed
        // For example, you might want stages for testing, deploying, etc.
    }

    // Add post-build actions if necessary
    // For example, you can archive the artifacts or trigger other jobs.
    // post {
    //     always {
    //         archiveArtifacts artifacts: 'target/*.jar', fingerprint: true
    //     }
    // }
}
