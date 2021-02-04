node {
    stage 'Code Checkout'
	checkout scm
    
    stage 'Build'
    bat "mvnw clean package"
    
    step([$class: 'JUnitResultArchiver', checksName: '', testResults: 'target/surefire-reports/TEST-*.xml'])
}