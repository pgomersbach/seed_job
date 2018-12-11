def giturl = 'https://github.com/pgomersbach/test2-source.git'
def gitbranch = 'master'

node {
    stage('get job definition, wait for slave') {
        checkout([$class: 'GitSCM',
            branches: [[name: "${gitbranch}"]],
            extensions: [[$class: 'WipeWorkspace']],
            userRemoteConfigs: [[url: "${giturl}"]]
        ])
    }
    withEnv(["SLACK_URL=https://hooks.slack.com/services/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s","DOCKER_REGISTRY=https://registry.hub.docker.com/v2","GITURL=${giturl}","GITBRANCH=${gitbranch}"]) {
        load './Jenkinsfile'
    }
}
