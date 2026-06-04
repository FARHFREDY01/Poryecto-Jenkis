stage('Test Oracle') {
    steps {
        sh '''
        export PATH=$PATH:/u01/app/oracle/product/12.2.0/client/bin
        sqlplus -S system/systemd@//192.168.1.8:1521/oemdb <<EOF
        select sysdate from dual;
        exit;
        EOF
        '''
    }
}
