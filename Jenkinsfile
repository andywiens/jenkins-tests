pipeline {
    agent { docker 'ruby' }
    stages {
        stage('build') {
            steps {
                sh 'ruby --version'
            }
        }
        stage("sanity") {
            steps {
                input "are we ready?"
            }
        }
        stage('test') {
            steps {
                sh 'uname -r'
                sh 'echo "hello andy"'
            }
        }
    }
    post {
        always {
            echo "well... we're finished"
        }

        success {
            echo "wooohooooo!!"
        }

        failure {
            echo "fuck"
        }
    }
}
