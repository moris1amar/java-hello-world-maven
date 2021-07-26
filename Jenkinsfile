pipeline {
    agent { 
        docker { 
            image 'maven:3.3.9' 
            args '-i --entrypoint='
        } 
    }
    stages {
        stage('Compile Hello World') {
            environment {
                  HOME="."
                }
            steps {
                git branch: 'main',
                    url: 'https://github.com/moris1amar/java-hello-world-maven.git'
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
