#!groovy

// Load shared pipeline libraries
@Library(['velox']) _

properties([buildDiscarder(logRotator(artifactDaysToKeepStr: '', artifactNumToKeepStr: '', daysToKeepStr: '14', numToKeepStr: ''))]);


veloxPipeline(slackChannel: who.builds.channel, nodeVersion: '10', npmVersion: '^6.9.0') { p ->



}

}
