pipeline {
    agent { 
            label "slave-2"      
    }
    stages {
        stage ('Compile Stage') {

            steps {
                    sh 'sudo yum install git -y'
                    sh 'yum git remote add origin 
                    sh 'sudo yum install maven -y'
                    sh 'sudo mvn install '
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
