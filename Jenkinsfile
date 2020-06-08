pipeline {
    agent any
    stages {
        stage('Example') {
            input {
                message "Should we continue?"
                ok "Yes, we should."
                submitter "alice,bob"
                parameters {
                    string(name: 'PERSON', defaultValue: 'Zul', description: 'Who should I say hello to?')
                }
            }
            when {
                equals expected: "Zul", actual: "${PERSON}"
            }
            steps {
                echo "Hello, ${PERSON}, nice to meet you."
            }
        }
    }
}
