pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'echo "Build...."'
        echo 'Build Complete'
        sleep 20
        echo 'Finished'
        sh 'echo "It is complete"'
      }
    }
    stage('test') {
      steps {
        sh 'echo "Testing in progress"'
        echo 'Testing complete'
        node(label: 'node1') {
          sh 'echo " Lets play more"'
          node(label: 'node2') {
            echo 'Running on node 2'
            sh 'hostname2=`hostname`'
          }

        }

      }
    }
    stage('Deploy') {
      steps {
        sh 'echo " Deploying"'
      }
    }
    stage('Finished') {
      steps {
        echo 'Finished with pipeline'
      }
    }
  }
}