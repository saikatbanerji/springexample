node('slave') {
   def mvnHome
   stage('Git') { // for display purposes
      // Get some code from a GitHub repository
      git 'https://github.com/saikatbanerji/springexample.git'
      // Get the Maven tool.
      // ** NOTE: This 'M3' Maven tool must be configured
      // **       in the global configuration.           
      mvnHome = "/usr/share/maven"
   }
   stage('Build_SONAR_NEXUS') {
      // Run the maven build
     sh 'mvn -f pom.xml -P spring-deploy clean deploy sonar:sonar'

   }
}
