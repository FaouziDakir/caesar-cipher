pipeline {
    agent any
    stages {
        stage("clone"){
            steps {
                sh "rm -rf *"
                sh "git clone https://github.com/FaouziDakir/caesar-cipher"
            }
        }
    }
    post{
            always {
                junit '**/caesar-cipher/build/test-results/test/TEST-*.xml'
            }
        }
}
