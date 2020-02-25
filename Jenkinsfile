#! groovy
// ^ include this shebang line so editors know the syntax is Groovy. It does
// nothing else.

/*
 * Build gateway-director-scale-test
 */
// Load common Groovy code
/*git = library('bmxNative').jenkinsLibs.Git.new()
artifactory = library('bmxNative').jenkinsLibs.ArtifactoryHelper.new()
docker = library('bmxNative').jenkinsLibs.Docker.new()
node = library('bmxNative@master').jenkinsLibs.Node.new()*/
properties([
  buildDiscarder(logRotator(artifactDaysToKeepStr: '', artifactNumToKeepStr: '', daysToKeepStr: '14', numToKeepStr: '')),
/*  parameters([
    // gives us an program-friendly string params
    string(name: 'build_label', defaultValue: 'gwd-scale', description: 'Specify the where the build runs. If set overrides the default'),
    string(name: 'dp_release', defaultValue: 'apic-gw-svc-develop-branch', description: 'Specify the datapower release rel-2018-4-1-branch, or apic-gw-svc-develop-branch'),
    string(name: 'branch_name', defaultValue: 'develop', description: 'Specify the branch of GwD and Gateway Director Test'),
    string(name: 'environment', defaultValue: 'datapower, apigateway', description: 'datapower, apigateway - Specify which environment to run the scale test against - default to both'),
    string(name: 'testcases', defaultValue: '35KAPIs, 1Kproducts, 10Ksubscriptions', description: '35KAPIs, 1Kproducts, 10Orgsw10Catalogs, 10Ksubscriptions - Specify which testcase to run - default to 35KAPIs, 1Kproducts, 10Ksubscriptions'),
    string(name: 'build_env', defaultValue: 'jenkins', description: 'DO NOT MANUALLY OVERRIDE.  Valid override value is "ab" which triggers testing of images (without GWD overlay) from ab pipeline')
  ]),
  pipelineTriggers([cron('0 0 * * *')]),
  disableConcurrentBuilds()*/
])

// Load shared pipeline libraries
@Library(['velox']) _

echo 'Build is  ${env.BRANCH_NAME}' 


veloxPipeline(slackChannel: 'test', nodeVersion: '10', npmVersion: '^6.9.0') { p ->

p.common {

  stage ('build') {


      try {
        captureNPMLogs {
          sh('npm install --prefer-offline')
        }
      } catch (Throwable e) {
        throw new Exception("FAIL install deps ]] ${e.dump()}")
      }

  sh  'npm run-script build'
    echo ' Build completed successfully'
  }


}

}
