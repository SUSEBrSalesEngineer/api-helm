stage 'Clonando o repositorio'
 node() {
  deleteDir()
  checkout scm
 }

stage 'Verificando vulnerabilidades com Neuvector'
neuvector nameOfVulnerabilityToExemptFour: '', nameOfVulnerabilityToExemptOne: '', nameOfVulnerabilityToExemptThree: '', nameOfVulnerabilityToExemptTwo: '', nameOfVulnerabilityToFailFour: '', nameOfVulnerabilityToFailOne: '', nameOfVulnerabilityToFailThree: '', nameOfVulnerabilityToFailTwo: '', numberOfHighSeverityToFail: '1', numberOfMediumSeverityToFail: '', registrySelection: 'Harbor', repository: '', scanLayers: true, scanTimeout: 10, tag: 'latest'
