pipeline {
    agent any
    
    stages {
        stage('greetings') {
            steps{
                echo 'Holla Mundos!'
            }
        }
	stage('preparation') {
		steps{
			echo 'hello preparation'
		}
	}
	stage('build') {
		steps{
			sh './gradlew clean test jar'
		}
	}
	stage('results'){
		steps{
			junit '**/build/test-results/test/TEST-*.xml'
		}
	}

    }
}

