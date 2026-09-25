pipeline {
    agent any

    tools {
        maven 'Maven-3.9.16'
    }
    
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
                    which mvn

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
