pipeline {
    options {
        disableConcurrentBuilds()
    }
    
    agent any

    environment {
        BUILD_URL = "${BUILD_URL}"
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building project...'
            }
        }
        stage('Test') {
            steps {
                echo 'Running tests...'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploy project...'
            }
        }
        }
        step([$class: 'InfluxDbPublisher',
            customData: null,
            customDataMap: null,
            customPrefix: null,
            target: 'local influxDB'])
    }

def assignURL(build_url) {
    def buildURL = [:]
    buildURL['url'] = build_url
    return buildURL
}
