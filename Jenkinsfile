#!groovy

node {
	   
	stage('Checkout'){

          checkout scm
       }

       stage('BuildArtifact'){
	       def mvn_version = 'M2_HOME'
               withEnv( ["PATH+MAVEN=${tool mvn_version}/bin"] ) 
	       {

         // sh 'mvn install'
	       
	       sh 'mvn clean'
       }
	       
       }
	   
      stage('Sonar') {
	      def mvn_version = 'M2_HOME'
               withEnv( ["PATH+MAVEN=${tool mvn_version}/bin"] ) 
	      {
                    //add stage sonar
                   // sh 'mvn sonar:sonar'
                }
      }
	
       
}
