pipeline {
    agent any
    stages {
        stage ('vcs') {
            steps {
                git url: 'https://github.com/pawanks434/MusicStore.git',
                    branch: 'main'
            }
        }
        stage ('build') {
            steps {
                sh 'dotnet restore ./MusicStore/MusicStore.csproj && dotnet build ./MusicStore/MusicStore.csproj'
            }
        }
        stage ('test') {
            steps {
                sh 'dotnet test ./MusicStoreTest/MusicStoreTest.csproj'
            }
        }
    }
}