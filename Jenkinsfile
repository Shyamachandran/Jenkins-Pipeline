pipeline {
    agent any
    stages {
        stage("Build") {
            steps {
                echo "Building..."
                
            }
            post {
                success {
                    emailext subject: "Build Status - Success",
                            body: "The build was successful",
                            to: "s223178782@deakin.edu.au"
                }
                failure {
                    emailext subject: "Build Status - Failure",
                            body: "The build has failed",
                            to: "s223178782@deakin.edu.au"
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
                            to: "s223178782@deakin.edu.au"
                }
                failure {
                    emailext subject: "Test Status - Failure",
                            body: "Tests have failed",
                            to: "s223178782@deakin.edu.au"
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
                            to: "s223178782@deakin.edu.au"
                }
                failure {
                    emailext subject: "Code Analysis Status - Failure",
                            body: "Code analysis failed",
                            to: "s223178782@deakin.edu.au"
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
                            to: "s223178782@deakin.edu.au"
                }
                failure {
                    emailext subject: "Security Scan Status - Failure",
                            body: "Security scan failed",
                            to: "s223178782@deakin.edu.au"
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
                            to: "s223178782@deakin.edu.au"
                }
                failure {
                    emailext subject: "Staging Test Status - Failure",
                            body: "Staging integration tests failed",
                            to: "s223178782@deakin.edu.au"
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