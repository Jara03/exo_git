def VERSION
def TAGGED
def VCS_REF
def BUILD_DATE
def DOCKER_VERSION
def DOCKER_IMAGE

node{

stage("toto"){
checkout scm
}

stage('mvm'){
    sh 'mvn package -D skipTests'
    sh 'mvn test'
    }


stage("Checkout"){
    checkout scm
    if(env.TAG_NAME){
    TAGGED = true
    VERSION = env.TAG_NAME.substring(1)
    DOCKER_VERSION = VERSION
    } else {
    TAGGED = false
    VERSION = null
    DOCKER_VERSION = "snapshot"
    }

}

}