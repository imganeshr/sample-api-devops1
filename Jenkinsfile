pipeline {
  agent any
  stages {
    stage('Unit Test') {
      steps {
        sh 'mvn clean test'
      }
    }

    stage('Deploy to CloudHub') {

      steps {
        sh 'mvn clean package deploy -DmuleDeploy \
        -Dmule.version=4.2.2 \
        -Denv=test \
        -Denc.key=Mulesoft12345678 \
        -Danypoint.platform.client_secret=7e98Da909c1044FA817d70120E906Fc1 \
        -Danypoint.platform.client_id=dbc9962c166e47358914fa3d6fd506b8 \
        -Dapi.id=16275739'
      }
    }
  }
}
