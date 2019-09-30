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
             	   sh "mvn test"
            }
        }
        stage('Deploy') {
            steps {
                sh 'mvn publish'
            }
        }
    }
}
