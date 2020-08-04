pipeline {
    agent any

    stages {
        stage ('Compile Stage') {

            steps {
                echo 'This is our Compile Stage'
            }
        }
		
		stage('Dev Box Confirmation') {
            steps {
                input('Deploy to Dev Box ?')
            }
        }
		
		stage('Dev Box Stage') {
            when {
                not {
                     branch "master"
                }
            }
            steps {
                echo 'Dev Box Stage done'
            }
        }

        stage('QA Box Confirmation') {
            steps {
                input('Deploy to QA Box ?')
            }
        }
		
		stage('QA Box Stage') {
            when {
                not {
                     branch "master"
                }
            }
            steps {
                 echo 'QA Box Stage done'
            }
        }
		
		stage('Staging Box Confirmation') {
            steps {
                input('Deploy to Staging Box ?')
            }
        }
		
		stage('Staging Box Stage') {
            when {
                not {
                     branch "master"
                }
            }
            steps {
                 echo 'Staging Box Stage done'
            }
        }
    }
}
