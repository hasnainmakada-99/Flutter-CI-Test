pipeline{
    agent any
    
    stages{
        stage('Clone Repository'){
            steps{
             git 'https://github.com/hasnainmakada-99/Flutter-CI-Test'
            }
        }

        stage('Build the apk'){
            steps{
                sh 'flutter build apk'  
            }
        }
        
        stage('Archive'){
            steps{
                archivedArtifacts artifacts: 'build/app/outputs/apk/release/app-release.apk'
            }
        }
    }
}