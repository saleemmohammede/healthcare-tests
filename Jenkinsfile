pipeline {
    agent any
    
    stages {
        stage('Test') {
            steps {
                dir('/var/lib/jenkins/workspace'){
                sh 'docker run -t --rm -v "$(pwd)": /var/lib/jenkins/katalonrunengine katalonc.sh -projectPath=/var/lib/jenkins/healthcare-tests.git -browserType="Chrome" -retry=0 -statusDelay=15 -testSuitePath="Test Suites/Jenkinsuite" -apiKey=46656da7-b8c5-45a3-90b4-5b587f8acf49'
                }
            }    
        }
    }
}
