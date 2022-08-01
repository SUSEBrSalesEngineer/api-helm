stage 'Clonando o repositorio'
 node() {
  deleteDir()
  checkout scm
 }

stage 'Verificando vulnerabilidades com Neuvector'
 node() {
  neuvector 
  numberOfHighSeverityToFail: '4',
  numberOfMediumSeverityToFail: '4',
  registrySelection: 'Harbor',
  repository: 'meu-projeto/nginx',
  scanLayers: true,
  scanTimeout: 2,
  tag: 'latest'
 }
