flag=true

pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                echo 'Building Project'
            }
        }
        stage('test') {
            steps {
                when {
                    expression {
                        flag == false
                    }
                }
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
