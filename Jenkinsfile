pipeline {
	agent any

	stages {
		stage('BUILD') {
			steps {
				checkout scm
				sh 'mvn -B -Dmaven.test.failure.ignore verify'
				junit '**/target/surefire-reports/TEST-*.xml'
			}
		}
	}
}