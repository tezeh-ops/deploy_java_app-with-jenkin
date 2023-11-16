@Library('my-shared-library') _

pipeline{

    agent any
    tools{
        maven "maven3.9.5"       //input the tool u are using
    }


    stages{
         
        stage('Git Checkout'){
                    //when { expression {  params.action == 'create' } }
            steps{
            gitCheckout(
                branch: "main",
                url: "https://github.com/tezeh-ops/deploy_java_app-with-jenkin"
            )
            }
        }

        stage('Unit Test maven'){
         
         //when { expression {  params.action == 'create' } }

            steps{
               script{
                   
                   mvnTest()
               }
            }
        }
    }



}
