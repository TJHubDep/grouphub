pipeline {
  
  agent any
    
	stages {
        
		stage ('One') {
      
		      steps {
            
			echo 'hi this is Tejashri'
          
			  }
      
		  }
       
		 stage ('Two') {

		            steps{
       
			     input('Do you want to proceed?')
      
		      }
    
		    }
      
		  stage ('Three') {
       
		           when {
       
			        not{
                 
				  branch "master"
            
			             }
       
			      }
         
			  
			steps {
                
				echo "hi"
        
		      	     }
 	    
		   }
       
		 stage ('Four'){
           
			 parallel {
         
			       stage ('Unit Testing') {
  
				                  steps {
                     
						   echo "Running Unit testing"
        
					            }
        
					        }
             
			   stage ('integration testing'){
                   
					     agent {
                   
						     docker {
                  
							          reuseNode false
          
						                        image 'ubuntu'
                  
						                 }
           
					               }
          
					          steps {
                     
							   echo "Running Itegration test"
         
					               }
              
					  } 
}
}
}  
           
}
