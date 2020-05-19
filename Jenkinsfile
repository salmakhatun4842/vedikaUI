  
node(){
    stage('Git checkout') {
        git 'https://github.com/salmakhatun4842/Vedika-UI.git'
    }
        
    stage('Install dependencies') {
        sh label: '', script: 'npm install'
        }
        
    stage('Build') {
        sh label: '', script: 'ng build --prod'
    }
     
stage('package build'){
  sh "tar -zcvf vedika.tar.gz dist/AngStr/"

 }
  
  stage('deploy artifacts'){
     sh label: '', script: '''scp  /var/lib/jenkins/workspace/vedikas/vedika.tar.gz root@34.228.217.4:/root/clone/vedikaUI
'''   
        }
}
