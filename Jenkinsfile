pipeline {
    agent { label 'nop'}
     tools {
        maven 'MAVEN_3.9.6' 
    }
    triggers {
      pollSCM('* * * * *')
    }
    stages {
        stage('git') {
            steps  {
                git url: 'https://github.com/ajaymaddela/game-of-lifeapr24.git'

            }
        }
        stage('build') {
            steps {
                
                sh 'mvn package'
            }
        }
    }
    
}