stage 'Clonando o repositorio'
 node() {
  deleteDir()
  checkout scm
 }

stage 'Verificando vulnerabilidades com Neuvector'
 node() {
  neuvector nameOfVulnerabilityToExemptFour: '', nameOfVulnerabilityToExemptOne: '', nameOfVulnerabilityToExemptThree: '', nameOfVulnerabilityToExemptTwo: '', nameOfVulnerabilityToFailFour: '', nameOfVulnerabilityToFailOne: '', nameOfVulnerabilityToFailThree: '', nameOfVulnerabilityToFailTwo: '', numberOfHighSeverityToFail: '1', numberOfMediumSeverityToFail: '1', registrySelection: 'Harbor', repository: 'meu-projeto/nginx', scanLayers: true, scanTimeout: 2, tag: 'latest'
 }
