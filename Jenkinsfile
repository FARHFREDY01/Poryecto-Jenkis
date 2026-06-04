pipeline {
    agent any

    stages {

        stage('Test Oracle') {
            steps {
                sh '''
                echo "Conectando a Oracle..."

                /u01/app/oracle/product/12.2.0.1/bin/sqlplus -S system/system@//192.168.1.8:1521/oemdb <<EOF
                select sysdate from dual;
                exit;
                EOF
                '''
            }
        }

    }
}
