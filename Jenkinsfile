node
  {
   def mavenHome = tool name: 'maven3.6.3'
  stage('1.git clone')
  {
  git credentialsId: 'GitCredentials', url: 'https://github.com/LandmakTechnology/maven-web-app'
  }
  stage('2.maven-Build')
  { 
    sh '${mavenHome}/bin/mvn clean package'
  }
  stage('3.CodeQualityReport')
  {
 // sh '${mavenHome}/bin/mvn sonar:sonar'
  }
 stage('4.UploadWarNexus')
        {
        //sh '${mavenHome}/bin/mvn clean deploy'
        }
 stage('5.DeployTomcat')
        {
       // deploy adapters: [tomcat9(credentialsId: 'Tomcat_Credentials', path: '', url: 'http://3.85.28.18:7777/')], contextPath: null, war: '**/*.war'
        }   
  } 
