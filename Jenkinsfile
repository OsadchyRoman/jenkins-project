pipeline {

	parameters {
		string(name: 'buildTool', defaultValue: 'Maven')
	}
    agent any
    tools {
        maven 'Maven 3.3.9'
        jdk 'jdk8'
    }
    stages {
        stage('Build') { 
            steps {
				echo "${params.buildTool}"
                bat "mvn -B -DskipTests clean package" 
            }
        }
    }
}