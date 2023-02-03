pipeline{
    agent any
    options{
        skipStageAfterUnstable()
    }
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

        stage("Artifacts archived")
        {
            steps
            {
                archiveArtifacts artifacts: 'build/app/outputs/apk/release/app-release.apk',
                
            }
        
        }
    
    }
}