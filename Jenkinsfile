pipeline {
    agent any

    tools {
        maven 'localmaven'
    }
    stages{
        stage('Build'){
            steps {
                bat 'mvn archetype:generate'
            }
            post {
                success {
                    echo 'Now Archiving........'
                    archiveArtifacts artifacts: '**/target/*.war'

                }
            }
        }
    }
}
