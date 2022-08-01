stage 'Clonando o repositorio'
 node() {
  deleteDir()
  checkout scm
 }

stage 'Bump Version — Using build#' {
 when { branch “${sourcecodeBranch}” }
steps {
 script
 {
 appVersion = “test-${BUILD_NUMBER}” 
 buildNumber = BUILD_NUMBER
 }
 }
 }
