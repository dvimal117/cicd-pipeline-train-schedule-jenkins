pipeline{
  agent any
  stages{
    stage ('Build'){
      git credentialsId: 'trainid', url: 'https://github.com/dvimal117/cicd-pipeline-train-schedule-jenkins'
      echo 'Running build automation'
      sh './gradlew build --no-daemon'
      archiveArtifacts 'dist/trainSchedule.zip'
    }
  }
}
