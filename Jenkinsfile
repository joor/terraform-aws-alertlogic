#!/usr/bin/env groovy
library "jenkins-library"


try {
  podTemplate(yaml: libraryResource('pod_templates/node.yaml'),label:'helmfiles-node'){
    node('helmfiles-node'){
      container('node'){
        semanticRelease.runSemanticReleaseStage()
      }
    }
  }
}catch (e) {
throw e
}
