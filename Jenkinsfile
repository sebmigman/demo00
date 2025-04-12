node {
    stage('Build') {
        docker.withClient {
            def mavenImage = docker.image('maven:3.8.5-openjdk-17')
            mavenImage.inside {
                sh 'mvn clean package'
            }
        }
    }
    stage('Test') {
        docker.withClient {
            def mavenImage = docker.image('maven:3.8.5-openjdk-17')
            mavenImage.inside {
                sh 'mvn test'
            }
        }
    }
}
