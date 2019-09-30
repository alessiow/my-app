pipeline { 
    agent any 
    options {
        skipStagesAfterUnstable()
    }
    stages {
        stage('Build') { 
            steps { 
                sh 'mvn clean' 
            }
        }
        stage('Test'){
            steps {
                sh 'mvn check'
                junit 'reports/my-app/pom.xml' 
            }
        }
        stage('Deploy') {
            steps {
                sh 'mvn make publish'
            }
        }
    }
}
