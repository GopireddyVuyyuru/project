pipeline {
    agent any

    stages {
        stage('Vaidation') {
            steps {
                echo 'Validate Project..'
		sh 'mvn validate'
		sh 'mvn compile'
            }
        }
        stage('UnitTest') {
            steps {
                echo 'Testing..'
		sh 'mvn test'
            }
        }
        stage('SonarAnalysis') {
            steps {
                echo 'Sonar Analysis....'
		sh 'mvn sonar:sonar -Dsonar.host.url=http://3.83.214.21:9000 -Dsonar.login=c8f34b0eb23db1a8c3483a138ba8272d3115d72b'
            }
        }
    }
}
