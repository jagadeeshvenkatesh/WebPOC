
node  
{       

    checkoutProject()
         
	}   
  catch (Exception e) {
       		
		throw e // So the build is considered a 'failure'
	}
} 

def checkoutProject() {

	stage ('Checkout Project from Stash') {
		// Always check out the main repository, to grab any potential recent changes/pushes
	  //checkout([$class: 'GitSCM', branches: [[name: '*/develop']], doGenerateSubmoduleConfigurations: false, extensions: [[$class: 'RelativeTargetDirectory', relativeTargetDir: "."]], submoduleCfg: [], userRemoteConfigs: [[credentialsId: 'a6d91d03-3dc0-475d-b286-1d606a1d7aac', url: "https://P2714819@stash.dev-charter.net/stash/scm/lin/performance-automation.git"]]])
    checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [[$class: 'RelativeTargetDirectory', relativeTargetDir: "."]], submoduleCfg: [], userRemoteConfigs: [[url: "https://github.com/TacoCTS/WebPOC.git"]]])
    //sh("aws s3 cp s3://seperf-workspace/Mjolnir/Profiles/AppEdge.txt /var/lib/jenkins/workspace/Lineup-PT-CICD-Main/service-config/AppEdge.txt || true")
    //sh ("chmod 777 ./property-files/configload.sh")
    }
	}
