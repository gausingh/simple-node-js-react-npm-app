#!groovy

properties([buildDiscarder(logRotator(artifactDaysToKeepStr: '', artifactNumToKeepStr: '', daysToKeepStr: '14', numToKeepStr: ''))]);

node {
    stage('checkout') {
        checkout scm
    }
    stage('build') {
        def docker = docker.image();
        echo ${docker}
    }
}