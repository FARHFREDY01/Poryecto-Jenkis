pipeline {
    agent any

    stages {
        stage('Test Oracle') {
            steps {
                sh '''
                echo "Conectando a Oracle..."
                sqlplus -S system/system@//192.168.1.8:1521/oemdb <<EOF
                SELECT SYSDATE FROM DUAL;
                EXIT;
                EOF
                '''
            }
        }
    }
}
