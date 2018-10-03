pipeline {
    agent any
     environment {
    def branch = 'master'
}
    stages {
        stage('Import Dev Code Streamsets') {
            steps {
                    script {	
        echo 'Obteniendo codigo fuente de Git ' 
        git(url: 'https://github.com/MarcoTulioGT/CSTMR_VW_DTL_SMS.git', branch:  branch)
                }
            }
        }
    }
}
