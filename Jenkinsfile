pipeline {
    agent {
        docker { image 'node:18' } // Menggunakan image Node.js versi 18
    }

    stages {
        stage('Clone Repository') {
            steps {
                git url: 'https://github.com/KeboSantet/docker-project.git', branch: 'main'
            }
        }

        stage('Build') {
            steps {
                sh 'npm install'
            }
        }

        stage('Test') {
            steps {
                sh 'npm test'
            }
            post {
                success {
                    echo 'Tes berhasil!'
                }
                failure {
                    echo 'Tes gagal!'
                }
            }
        }

        stage('Deploy') {
            steps {
                echo 'Menjalankan aplikasi...'
                sh 'nohup node app.js &'
            }
        }
    }
}
