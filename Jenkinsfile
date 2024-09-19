pipeline { 
            agent any
            parameters { string defaultValue: 'develop', description: 'This is branch name for repository', name: 'branch_name' }

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
