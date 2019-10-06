pipeline {
         agent any
         stages {
            stage('prepare') {
                steps {
                    echo 'preparing the build'
                }
            }
                stage('input') {
                    input {
                        message "Should we continue?"
                        ok "Yes, we should."
                        submitter "peter"
                        parameters {
                            string(name: 'PERSON', defaultValue: 'name', description: 'Who should I say hello to?')
                        }
                    }
                steps {
                    echo "Hello, ${PERSON}, nice to meet you."
                    }
                }
                stage('Example Deploy') {
                    when {
                        branch 'production'
                    }
                    steps {
                        echo 'Deploying'
                    }
                }
            }
    }
