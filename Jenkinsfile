node {
    timestamps {
        try {
            checkout scm
            stage("Say Hello") {
                script {
                    ansiColor('xterm') {
                        sh """
                        ls -lh
                        chmod +x hello-world.sh
                        hello-world.sh
                        """
                    }
                }
            }
            currentBuild.result = 'SUCCESS'
        } catch (Exception err) {
            currentBuild.result = 'FAILURE'
        }
    }
}