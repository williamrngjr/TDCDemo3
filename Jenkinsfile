pipeline {
  agent any
  stages {
    stage('Stage1') {
      steps {
        parallel(
          "Stage1": {
            echo 'Stage 1'
            
          },
          "Stage1B": {
            echo 'Stage1B'
            
          }
        )
      }
    }
    stage('Stage2') {
      steps {
        parallel(
          "Stage2": {
            echo 'Stage2'
            
          },
          "Stage3": {
            echo 'Stage3'
            
          },
          "Stage4": {
            echo 'Stage4'
            
          }
        )
      }
    }
    stage('AllocateNode') {
      steps {
        parallel(
          "AllocateNode": {
            node(label: 'Node1') {
              echo 'Inside Node'
            }
            
            
          },
          "": {
            echo 'AllocateNodeBelow'
            
          }
        )
      }
    }
  }
  environment {
    NAME = 'WILLIAM'
    TEAM = 'TDC'
  }
}