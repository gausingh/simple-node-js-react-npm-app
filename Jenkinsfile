#!groovy

// Load shared pipeline libraries
@Library(['velox', 'velox-goa']) _

properties([buildDiscarder(logRotator(artifactDaysToKeepStr: '', artifactNumToKeepStr: '', daysToKeepStr: '14', numToKeepStr: ''))]);

veloxPipeline() {
    echo 'Test Message';
}