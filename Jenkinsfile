def registryProject='harbor.demo.gbrlins.com/meu-projeto'
def IMAGE="${registryProject}/nginx:${env.BUILD_ID}"

stage ('Clonando o repositorio'){
  deleteDir()
  checkout scm
 }

def img = stage('Build'){
  docker.build("$IMAGE", '.')
}

stage ('Push to registry'){
  docker.withRegistry("$IMAGE", 'reg1'){
   img.push 'latest'
   img.push()
}
  
stage 'Verificando vulnerabilidades com Neuvector'
 node() {
  neuvector nameOfVulnerabilityToExemptFour: '', nameOfVulnerabilityToExemptOne: '', nameOfVulnerabilityToExemptThree: '', nameOfVulnerabilityToExemptTwo: '', nameOfVulnerabilityToFailFour: '', nameOfVulnerabilityToFailOne: '', nameOfVulnerabilityToFailThree: '', nameOfVulnerabilityToFailTwo: '', numberOfHighSeverityToFail: '', numberOfMediumSeverityToFail: '', registrySelection: 'Harbor', repository: 'meu-projeto/nginx', scanLayers: true, scanTimeout: 10, tag: 'latest'
 }
