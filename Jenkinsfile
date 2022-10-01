pipeline {
    agent any

    stages {
//       stage('Git chekout') {
//            steps {
//              git branch: 'main', url: 'https://github.com/codersanty2/gitjenkinsintegration'
//            }
//        }
        stage('run python file') {
            steps { 
                sh 'python3 myfile.py > /tmp/file1.txt'   
            }
        }
        stage('Add date to the final file') {
            steps { 
                sh 'date >> /tmp/file1.txt'   
            }
        }
        stage('Make artifacts') {
            steps { 
                sh 'make'   
                archiveArtifacts artifacts: '/tmp/file2', followSymlinks: false
            }
        }
    }
}

