pipeline {

	parameters {
		string(name: 'buildTool', defaultValue: 'Maven')
	}
    agent {
        docker {
            image 'maven:3-alpine' 
            args '-v /root/.m2:/root/.m2' 
        }
    }
    stages {
        stage('Build') { 
            steps {
				echo "${params.buildTool}"
                sh 'mvn -B -DskipTests clean package' 
            }
        }
    }
}