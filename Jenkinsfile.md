## Jenkins Pipeline:

=> There are GUI and Pipeline as code available
=> Jenkinsfile can be witten as Scripted or Declarative. Scripted syntax use groovy script and Declarative syntax declarative command (recent addition)

```Jenkinsfile
pipeline {
    agent any

    stages {
        stage("build") {
            steps {

            }
        }
    }
}

node {
    // groovy syntax
}
```