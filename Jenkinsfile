pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Running build automation'
                sh './gradlew build --no-daemon'
                archiveArtifacts artifacts: 'dist/trainSchedule.zip'
            }
        }
        stage('Staging'){
              steps {
                 sh 'ls' 
              }
        }
        stage('Prod'){
              steps {
                 input message:'Approve deployment?'
                 sh 'ls' 
              }
        }
    }
}
