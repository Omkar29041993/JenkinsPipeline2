pipeline {
    agent any
    parameters {
        gitParameter name: 'REVISION', 
                     type: 'PT_REVISION',
                     defaultValue: 'master'
    }
    stages {
        stage('Example') {
            steps {
                checkout([$class: 'GitSCM', 
                          branches: [[name: "${params.REVISION}"]], 
                          doGenerateSubmoduleConfigurations: false, 
                          extensions: [], 
                          gitTool: 'Default', 
                          submoduleCfg: [], 
                          userRemoteConfigs: [[url: 'https://github.com/Omkar29041993/Rollback']]
                        ])
            }
        }
    }
}
