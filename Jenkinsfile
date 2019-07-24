pipeline {
	agent any

	stages {
		stage('BUILD') {
			steps {
				checkout scm
				container('maven') {
				  sh 'mvn -B -ntp -Dmaven.test.failure.ignore verify'
				}
				junit '**/target/surefire-reports/TEST-*.xml'
			}
		}
	}
}