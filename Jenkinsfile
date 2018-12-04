def giturl = 'https://github.com/pgomersbach/test-source.git'
def gitbranch = 'master'

node {
    stage('get job definition, wait for slave') {
        checkout([$class: 'GitSCM',
            branches: [[name: "${gitbranch}"]],
            extensions: [[$class: 'WipeWorkspace']],
            userRemoteConfigs: [[url: 'https://github.com/pgomersbach/test-source.git']]
        ])
    }
    load './Jenkinsfile'
}
