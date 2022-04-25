pipeline{
  agent any
  stages{
    stage ('git'){
      echo 'branch comit'
      steps{
        git credentialsId: 'trainid', url: 'https://github.com/dvimal117/cicd-pipeline-train-schedule-jenkins'
      }}
    stage ('Build'){
      steps{
        echo 'Running build automation'
        sh './gradlew build --no-daemon'
        archiveArtifacts 'dist/trainSchedule.zip'
      }
    }
  }
}
