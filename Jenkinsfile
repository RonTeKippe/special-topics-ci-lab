
node {
  stage('checkout sources') {
        // You should change this to be the appropriate thing
        git url: 'https://github.com/RonTeKippe/special-topics-ci-lab'
  }

  stage('Build') {
    // you should build this repo with a maven build step here
    try {
        withMaven (maven: 'maven3') {
          sh "mvn package"
          }
        }finally{
        junit 'target/**/*.xml'
        }
        echo "hello"
      }
}
