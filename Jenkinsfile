pipeline {
<<<<<<< HEAD
    agent any

    stages {
        stage('Clone Repo') {
=======
    agent {
        docker { image 'node:18' } // Memastikan Jenkins pakai image yang punya Node.js
    }

    stages {
        stage('Clone Repository') {
>>>>>>> 049e42a (Initial commit with Jenkinsfile)
            steps {
                git url: git 'https://github.com/KeboSantet/docker-project.git', branch: 'main'
            }
        }

        stage('Build') {
            steps {
<<<<<<< HEAD
                echo 'Tahap build berjalan.'
=======
                sh 'npm install'
>>>>>>> 049e42a (Initial commit with Jenkinsfile)
            }
        }

        stage('Test') {
            steps {
<<<<<<< HEAD
                echo 'Tes unit berjalan (simulasi).'
=======
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
>>>>>>> 049e42a (Initial commit with Jenkinsfile)
            }
        }
    }
}
