pipeline {
    agent any

    stages {
        stage('Test Oracle') {
            steps {
                sh '''
                echo "Conectando a Oracle..."

                ssh oracle@192.168.1.8 "
                source ~/.bash_profile;
                sqlplus -S system/system@oemdb <<EOF
                select sysdate from dual;
                exit;
                EOF
                "
                '''
            }
        }
    }
}
