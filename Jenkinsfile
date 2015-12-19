// see http://jenkins-ci.org/content/pipeline-code-multibranch-workflows-jenkins
node {
   // Mark the code checkout 'stage'....
   stage 'Checkout'

   // Checkout code from repository
   checkout scm
   stage 'Build'

   step([$class: 'ArtifactArchiver', artifacts: 'README.md', fingerprint: true])
   step([$class: 'ArtifactArchiver', artifacts: 'does_not_exist', fingerprint: true])

}