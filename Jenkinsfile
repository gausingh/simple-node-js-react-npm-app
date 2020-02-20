#!groovy

// Load shared pipeline libraries
@Library(['velox']) _

properties([buildDiscarder(logRotator(artifactDaysToKeepStr: '', artifactNumToKeepStr: '', daysToKeepStr: '14', numToKeepStr: ''))]);

veloxPipeline() {
    echo 'Test Message';
}