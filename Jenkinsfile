node{

stage("toto"){
checkout scm
}

stage('mvm'){
    sh 'mvn package -D skipTests'
    sh 'mvn test'
}
}