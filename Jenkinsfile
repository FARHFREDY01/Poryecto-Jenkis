pipeline {
    agent any

    stages {

        stage('Test Oracle') {
            steps {
                sh '''
                echo "Conectando a Oracle..."
                sqlplus -S system/password@//IP:1521/SERVICE <<EOF
                select sysdate from dual;
                exit;
                EOF
                '''
            }
        }

    }
}
