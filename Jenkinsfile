@Library('jenkinsfile-shared-library@main') _

def config = readYaml text: """
  APP: 'Demo'
  VERSION: 'v5'
  DOCKER_IMAGE: 'manu756/app_for_demo'
  DOCKERFILE_LOCATION: 'app/.'
  SVC_NAME: 'nodejs-app'
"""

config.keySet().each {
    env."${it}" = config[it]
}

"${pipelineSelector(env)}"(env)
