pipeline {
    agent {
        docker {
            image 'node:7-alpine'
        }
    }
    stage 'Prepare Container'
    stage 'Install Gems'
    stage 'Prepare Database'
    stage 'Invoke Rake'
    stage 'Security scan'
    stage 'Deploy'
}
