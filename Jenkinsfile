pipeline{
  agent any
  stages{
    stage ('Build'){
      echo 'Running build automation'
      sh './gradlew build --no-daemon'
      archiveArtifacts 'dist/trainSchedule.zip'
    }
  }
}
