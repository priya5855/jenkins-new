pipeline {
 agent any
stages {
stage ('checkout source code') {
steps {
 	//get source code from git repository
	}
}
stage ('Build') {
steps {
	//run the following maven command
sh "export PATH=$PATH:/opt/maven/bin"
sh "source /etc/profile"
sh "mvn Dmaven.test.failure.ignore=true clean package"
}
}
}
}
