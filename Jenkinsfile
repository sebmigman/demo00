pipeline {
    agent any // Run on any available agent

    stages {
        stage('Test Configuration') {
            steps {
                echo 'Jenkins configuration is working!'
            }
        }
        stage('Test Docker') {
            steps {
                script {
                    try {
                        // Run the hello-world Docker image
                        docker.image('hello-world').run()
                    } catch (Exception e) {
                        echo "Error running Docker: ${e.getMessage()}"
                        error "Docker test failed"
                    }
                }
            }
        }
    }
}
