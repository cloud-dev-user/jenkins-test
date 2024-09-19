pipeline { 
            agent any
            stages{
                stage("checkout code") {
                    steps{
                        git branch: "$branch_name", url: 'https://github.com/cloud-dev-user/java-war-project.git'
                    }
                }
                stage("build code") {
                    steps{
                        sh 'mvn package'
                    }
                }
            }
}
