pipeline {
    agent any

    stages {
        stage('Run marks script') {
            steps {
                // Run python script and send output to artifacts.txt
                sh 'python3 marks.py > artifacts.txt'
            }
        }
    }

    post {
        always {
            // Archive artifacts.txt so you can download it from Jenkins
            archiveArtifacts artifacts: 'artifacts.txt', fingerprint: true
        }
    }
}

