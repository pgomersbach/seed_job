node {
    stage('get job definition, wait for slave') {
        checkout([$class: 'GitSCM',
            branches: [[name: 'master']],
            extensions: [[$class: 'WipeWorkspace']],
            userRemoteConfigs: [[url: 'https://github.com/pgomersbach/test-source.git']]
        ])
    }
    load './Jenkinsfile'
}
