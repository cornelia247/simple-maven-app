pipeline {

    agent any
    parameters {
        choice(name: "VERSION", choices: ['1.1.0', '1.2.0', '1.3.0'], description: '')
        booleanParam(name: 'executeTests', defaultValue: true, description: '')
    }
    stages {

        stage("build") {
            steps{
                echo "Building the application..."

            }
        }
        stage("test") {
            when {
                expression {
                    params.executeTests
                }
            }
            steps{
                echo "Testing the application..."
            }
        }
        stage("deploy") {
            steps{
                echo "Deploying the application..."
                echo "Deploying version ${params.VERSION}"
            }
        }
    }




































// pipeline {

//     agent any
//     environment {
//         NEW_VERSION = "1.3.0"
//     }
//     stages {

//         stage("build") {
//             steps{
//                 echo "Building the application..."
//                 echo "Building version ${NEW VERSION}"
//             }
//         }
//         stage("test") {
//             steps{
//                 echo "Testing the application..."
//             }
//         }
//         stage("deploy") {
//             steps{
//                 echo "Deploying the application..."
//                 withCredentials([
//                     usernamePassword(credentials: 'server-credentials', usernameVariable: USER, passwordVariable: PWD)
//                 ]) {
//                     sh "some script ${USER} ${PWD} "
//                 }
//             }
//         }
//     }
    // post {
    //     always {
    //         // alwlays executed after the build either passes or fails, i.e send a mail to the team about the build condition 
    //     }
    //     success {
    //         //run after success
    //     }
    //     failure {
    //         // after failure
    //     }
    // }
}











































// def gv

// pipeline {
//     agent any
//     stages {
//         stage("init") {
//             steps {
//                 script {
//                     gv = load "script.groovy"
//                 }
//             }
//         }
//         stage("build jar") {
//             steps {
//                 script {
//                     echo "building jar"
//                     //gv.buildJar()
//                 }
//             }
//         }
//         stage("build image") {
//             steps {
//                 script {
//                     echo "building image"
//                     //gv.buildImage()
//                 }
//             }
//         }
//         stage("deploy") {
//             steps {
//                 script {
//                     echo "deploying"
//                     //gv.deployApp()
//                 }
//             }
//         }
//     }   
// }