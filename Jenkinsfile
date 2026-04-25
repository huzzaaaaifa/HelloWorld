
pipeline {
    agent any
    environment {
        //variables defined here can be used by any stage
        NEW_VERSION = '1.3.0'
    }
    stages {
        stage('build') {
            steps {
                echo 'Building Project'
                //using environment variable
                //To output the value of variable in string use " "
                echo "Building version ${NEW_VERSION}"
            }
        }
        stage('test') {
            steps {
                echo 'Testing Project'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
    post {
        always {
            echo 'Post build condition running'
        }
        failure {
            echo 'Post Action if Build Failed'
        }
    }
}
