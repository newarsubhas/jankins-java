node{
	stage('SCM Checkout'){
		git 'https://github.com/prabhatpankaj/jankins-java'
	}
	stage('Compile-Package'){
		def mvnHome = tool name: 'maven-3', type: 'maven'
		sh "${mvnHome}/bin/mvn package"
	}
	stage('Email Notification'){
	mail bcc: '', body: 'helo body', cc: '', from: 'prabhatiitbhu@gmail.com', replyTo: '', subject: 'hello subject', to: 'prabhat@aptence.com'
	}
	stage('Slack Notification'){
	slackSend baseUrl: 'https://hooks.slack.com/services/', channel: '#devops', color: '#439FE0', message: 'Build Started: "${env.JOB_NAME}" "${env.BUILD_NUMBER}"', teamDomain: 'devops-dxa2539', tokenCredentialId: 'slack-secret'
	}

}
