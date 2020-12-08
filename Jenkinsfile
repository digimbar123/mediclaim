pipeline {
   agent any
	stages {
      stage('Git Checkout') {
         steps {
            git 'https://github.com/digimbar123/mediclaim'
		}
	}
    }
	stage('Build') {
		steps {
			withSonarQubeEnv('sonar3') {
				sh '/opt/maven/bin/mvn clean verify sonar:sonar'
			}
		}
	}

}
}
