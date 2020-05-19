  
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
     sh label: '', script: '''scp  /var/lib/jenkins/workspace/angualr/vedika.tar.gz root@:54.208.230.196/root/clone/vedikaUI
'''   
        }
}
