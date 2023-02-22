#!groovy
pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/wcouturiaux/forage-accenture-dev-adv-eng'
            }
        }
        stage('Build') {
            steps {
                sh './gradlew assemble'
            }
        }
        stage('Unit Test') {
            steps {
                sh './gradlew test'
            }
        }
    }
}