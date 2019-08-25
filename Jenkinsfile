#!/usr/bin/groovy
pipeline {
    agent none

    stages {
        stage('Testing') {
            parallel {
                stage('Test base') {
                    agent {
                        docker {
                            image 'quay.io/ansible/molecule'
                        }
                    }
                    steps {
                        dir('roles/base') {
                            sh 'molecule test'
                        }
                    }
                }
                stage('Test cli') {
                    agent {
                        docker {
                            image 'quay.io/ansible/molecule'
                        }
                    }
                    steps {
                        dir('roles/cli') {
                            sh 'molecule test'
                        }
                    }
                }
                stage('Test development') {
                    agent {
                        docker {
                            image 'quay.io/ansible/molecule'
                        }
                    }
                    steps {
                        dir('roles/development') {
                            sh 'molecule test'
                        }
                    }
                }
            }
        }
    }
}
