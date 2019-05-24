pipeline {
  agent {
    label 'tools'
  }
  
  stages{
    stage('current'){
      steps{
        container('tools'){
          script{
            alaudaDevops.withCluster(){
              def ns = alaudaDevops.selector('namespace')
              ns.withEach {
                echo "${it.name()}"
              }
            }
          }
        }
      }
    }
  }
}
