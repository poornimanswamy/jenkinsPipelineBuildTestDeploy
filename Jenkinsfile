node('master'){checkout([$class: 'GitSCM', branches: [[name: '*/master']], browser: [$class: 'GithubWeb', repoUrl: 'https://github.com/poornimanswamy/spring-petclinic'], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/poornimanswamy/spring-petclinic.git']]])
bat 'mvnw:cmd clean install'
bat '''cd dockercd internal-dbdocker build -t spring-petclinic .'''}
