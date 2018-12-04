node {
    checkout([$class: 'GitSCM',
        branches: [[name: 'master']],
        extensions: [[$class: 'WipeWorkspace']],
        userRemoteConfigs: [[url: 'https://github.com/pgomersbach/test-source.git']]
    ])
    load Jenkinsfile
}
