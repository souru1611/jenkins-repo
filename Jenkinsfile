pipeline {
    agent { 
            label "slave-1"      
    }
    stages {
        stage ('Compile Stage') {

            steps {
                
                    sh 'sudo mvn clean compile'
                }
            
        }

        stage ('Testing Stage') {

            steps {
                
                    sh 'sudo mvn test'
                }
            
        }


        stage ('Install Stage') {
            steps {
                
                    sh 'sudo mvn install'
                }
            
        }
        
        stage ('Echo Branch') {

            steps {
                
                    echo "This is master branch"
                }
            
        }
    }
}
