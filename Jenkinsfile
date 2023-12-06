pipeline {
	agent any

	stages {

		stage("build") {
        steps {
                echo "Build"
        }
        }

        stage("test") {
        steps {
                echo "Test"
        }
        }

        stage("deploy"){
         when {
            branch "main"
         }
         steps {
                echo "Deploy"
         }
        }

	}

}
