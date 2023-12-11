pipeline {
	agent any

	stages {

		stage("build") {
        steps {
                mvn clean compile
        }
        }

        stage("test") {
        steps {
                mvn test
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
