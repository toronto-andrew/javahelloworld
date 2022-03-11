pipeline {
  agent {
    node {
      label 'JavaNode1'
    }

  }
  stages {
    stage('stage1') {
      agent {
        node {
          label 'JavaNode1'
        }

      }
      steps {
        echo 'doing step1'
        git(url: 'https://github.com/toronto-andrew/javahelloworld.git', branch: 'master', credentialsId: 'toronto-andrew', poll: true)
        sh '''ls -l
cat README.md'''
      }
    }

  }
}