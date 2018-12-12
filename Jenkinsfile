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

}
