stage 'Clonando o repositorio'
 node() {
  deleteDir()
  checkout scm
 }

stage 'Verificando vulnerabilidades com Neuvector'
 node() {
  neuvector nameOfVulnerabilityToExemptFour: '', nameOfVulnerabilityToExemptOne: '', nameOfVulnerabilityToExemptThree: '', nameOfVulnerabilityToExemptTwo: '', nameOfVulnerabilityToFailFour: '', nameOfVulnerabilityToFailOne: '', nameOfVulnerabilityToFailThree: '', nameOfVulnerabilityToFailTwo: '', numberOfHighSeverityToFail: '', numberOfMediumSeverityToFail: '', registrySelection: 'Harbor', repository: 'meu-projeto/nginx', scanLayers: true, scanTimeout: 10, tag: 'latest'
 }
