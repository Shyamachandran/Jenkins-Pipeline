pipeline {
    agent any
    stages {
        stage("Build") {
            steps {
                echo "Building..."
                
            }
            post {
                success {
                    emailext attachLog: true,
                             subject: "Build Status - Success",
                            body: "The build was successful",
                            to: "shyama.nait@gmail.com"
                }
                failure {
                    emailext attachLog: true,
                             subject: "Build Status - Failure",
                            body: "The build has failed",
                            to: "shyama.nait@gmail.com"
                }
            }
        }
        
        stage("Unit and Integration Tests") 
        {
            steps {
                echo "Running unit and integration tests..."
            }
            post {
                success {
                    emailext subject: "Test Status - Success",
                            body: "All tests passed successfully",
                            to: "shyama.nait@gmail.com"
                }
                failure {
                    emailext subject: "Test Status - Failure",
                            body: "Tests have failed",
                            to: "shyama.nait@gmail.com"
                }
            }
        }
        
        stage("Code Analysis") {
            steps {
                echo "Performing code analysis..."
            }
            post {
                success {
                    emailext subject: "Code Analysis Status - Success",
                            body: "Code analysis passed",
                            to: "shyama.nait@gmail.com"
                }
                failure {
                    emailext subject: "Code Analysis Status - Failure",
                            body: "Code analysis failed",
                            to: "shyama.nait@gmail.com"
                }
            }
        }
        
        stage("Security Scan") {
            steps {
                echo "Performing security scan..."
            }
            post {
                success {
                    emailext subject: "Security Scan Status - Success",
                            body: "Security scan passed",
                            to: "shyama.nait@gmail.com"
                }
                failure {
                    emailext subject: "Security Scan Status - Failure",
                            body: "Security scan failed",
                            to: "shyama.nait@gmail.com"
                }
            }
        }
        
        stage("Deploy to Staging") {
            steps {
                echo "Deploying to staging server..."
            }
        }
        
        stage("Integration Tests on Staging") {
            steps {
                echo "Running integration tests on staging..."
            }
            post {
                success {
                    emailext subject: "Staging Test Status - Success",
                            body: "Staging integration tests passed",
                            to: "shyama.nait@gmail.com"
                }
                failure {
                    emailext subject: "Staging Test Status - Failure",
                            body: "Staging integration tests failed",
                            to: "shyama.nait@gmail.com"
                }
            }
        }
        
        stage("Deploy to Production") {
            steps {
                echo "Deploying to production server..."
                
            }
        }
    }
}
