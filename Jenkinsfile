pipeline {
	agent any
	 environment {
        // Define environment variables
        MAVEN_HOME = tool 'maven3' // Assumes Maven is configured in Jenkins tools
        // TOMCAT_URL = 'http://tomcat-user:tomcat-password@tomcat-server:8080'
        // TOMCAT_MANAGER_URL = "${TOMCAT_URL}/manager/text"
        // WAR_FILE = 'your-app.war' // Update with your actual WAR file name
    }
	
	stages {

		stage("build") {
        steps {
                bat "\"${MAVEN_HOME}\\bin\\mvn\" clean compile package"
        }
        }

        stage("test") {
        steps {
                bat "\"${MAVEN_HOME}\\bin\\mvn\" test"
        }
        }

        stage("deploy"){
         when {
            branch "main"
         }
         steps {
                echo "deployed"
         }
        }

	}

}
