pipeline {
agent {
 node { label 'master'}
}
tools {
 oc 'oc'
  }
 stages {
		  stage (' Create New project ' ) {
		    steps {
			 script {
			   openshift.withCluster ( CLUSTER_NAME ) {
			           openshift.newProject ( PROJECT_NAME)
					  }
					 }
					 }
				}
			stage ( ' Deploy App ')
			  steps{
			  scripts{
			  openshift.withCluster ( CLUSTER_NAME ) {
			          openshift.withProject ( PROJECT_NAME ) {
					             echo "Hello from project $(openshift.project()} in cluster $(openshift.cluster()}'
								 def created = openshift.newAPP( 'https
