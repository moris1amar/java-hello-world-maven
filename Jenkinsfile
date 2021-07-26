pipeline {
    agent { 
        docker { image 'maven:3.3.9' } 
        }
    stages {
        stage('Compile Hello World') {
            steps {
                git 'https://github.com/moris1amar/java-hello-world-maven'
                sh 'mvn --version'
                sh 'mvn clean install'
            }
        }
        stage('Run Hello World') {
            steps {
                sh 'java -cp target/hello-world-maven-0.1.0.jar hello.HelloWorld'
            }
        }
    } 
}
