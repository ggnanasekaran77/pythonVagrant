#!/usr/bin/env groovy

pipeline {
    agent any

    stages {
        stage('Python App from Vagrantfile') {
            steps {
                ansiColor ('xtrem') {
                     withEnv(['ANSIBLE_HOME=/opt/app/ansible/python27']) {
                           sh "chmod +x ansible-playbook;./ansible-playbook"
                     }
                }
            }
        }
    }
}
