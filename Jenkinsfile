pipeline {
    agent none
        environment {
        ENV_DOCKER = credentials('dockerhub')
        DOCKERIMAGE = "proserven/sample-spring-boot"
        EKS_CLUSTER_NAME = "demo-cluster"
    }
    stages {
        stage('build') {
            agent {
                docker { image 'openjdk:11-jdk' }
            }
            steps {
                // sh 'chmod +x gradlew && ./gradlew build jacocoTestReport'
                sh 'echo hello world'
            }
        }
        // stage('sonarqube') {
        // agent {
        //     docker { image 'sonarsource/sonar-scanner-cli' } }
        //     steps {
        //         sh 'echo scanning!'
        //     }
        // }
        // stage('docker build') {
        //     steps {
        //         sh 'echo docker build'
        //     }
        // }
        // stage('docker push') {
        //     steps {
        //         sh 'echo docker push!'
        //         }
        //     }
        // stage('Deploy App') {
        //     steps {
        //         sh 'echo deploy to kubernetes'               
        //     }
    // }
}

}