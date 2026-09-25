pipeline {
    agent any

    stages {
        stage('Environment') {
            steps {
                sh '''
                    echo "===== SYSTEM ====="
                    uname -a

                    echo "===== JAVA ====="
                    java -version || true

                    echo "===== MAVEN ====="
                    mvn --version || true

                    echo "===== PATH ====="
                    echo "$PATH"

                    echo "===== WORKSPACE ====="
                    pwd
                    ls -la
                '''
            }
        }
    }
}
