pipeline {
    agent { label 'nop'}
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
                sh 'cd ~/game-of-lifeapr24/'
                sh 'mvn package'
            }
        }
    }
    
}