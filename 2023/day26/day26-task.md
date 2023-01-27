# Day 26 - Task

- Declarative pipeline script for a simple `hello world` print purpose.

>Pipeline Script 
```
pipeline{
    agent any
    stages{
        stage(print){
            steps{
                sh 'echo "hello world" '
            }
        }
        stage(stage2){
            steps{
                sh 'echo "stage 2 completed" '
            }
        }
        stage(stage3){
            steps{
                sh 'echo "stage 3 completed"'
            }
        }
    }
}

```
