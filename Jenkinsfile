node {
   stage('Preparation') { // for display purposes
      // Get some code from a GitHub repository
      git 'https://github.com/KiranSonawane2003/time-tracker.git'
      // Get the Maven tool.
      // ** NOTE: This 'M3' Maven tool must be configured
      // **       in the global configuration.           
      sh 'npm install express'
      sh 'npm install moment'
      sh 'npm install ejs'
   }
   stage('Build') {
      // Run the maven build
         sh "node index.js"
   }
   stage('Results') {
      junit '**/target/surefire-reports/TEST-*.xml'
      archive 'target/*.jar'
   }
   
}
