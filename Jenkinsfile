pipeline {
  agent any
  environment {
    def branch = 'master'
}

  stages {
    stage('Get Git Code') {
      steps {
        script {	
        echo 'Obteniendo codigo fuente de Git ' 
        git(url: 'https://github.com/MarcoTulioGT/CSTMR_VW_DTL_SMS.git', branch:  branch)
                }
      }
    }

     stage('import Code dev') {
      steps {
        script {
           echo 'Desplegando aplicación para ambiente de ' + branch
		   if (branch=='Desarrollo') {
          echo 'Deploy Dev'
			}
		   if (branch=='QA') {
          echo 'Deploy QA'
			}
		   if (branch=='dev') {
  		 echo 'Deploy dev'
		   }					   
                }
            }
     }
    stage('Deploy to QA') {
     // when {
     //   environment name: 'TAG_ON_DEPLOY_PROD', value: 'yes'
     // }
      steps {
        script {
		   if (branch=='master') {
           echo 'Deploy QA'
                    }
		   }
                }
      }
    }
  }
}
