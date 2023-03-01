node('what is the label you give in jenkins') {
    stage('vcs') {
        git url : 'https://github.com/satya36-cpu/game-of-life.git',
        branch : 'master/main'
    }
    stage ('build') {
        sh export PATH = "usr/bin/jvm/java:$PATH"
    }
    stage('post build acion') {
      archive Artifacts 
        Artifacts : '**target/game of life.war'
    }
    stage('test result') {
        junit : '**/surefire-reports/TEST-*.xml'
    }   
}