280+ new messages

Loading history...


Q4120 Ersin SARI
  10:25 PM
hocam burda step demeden direk stage altına yazsak olur mu yoksa birden fazla stage olduğu için zorunlu mu ?


Q1147 Ali
  10:25 PM
uzantısını yazmayacak mıyız hocam hellonun


Q2157-Şerafettin
  10:25 PM
ilk stepsin altına sh diyip eklesek olmaz mı hocam
:white_check_mark:
1



PB113-Yunus Altay
  10:28 PM
debug ediyor
10:28
stepi gecmeden 2. ye baslamiyor


Q2141 Adem
  10:29 PM
hepte en heyacanlı bölümü sona saklıyorsunuz


Ramazan - Instructor
  10:30 PM
jenkins-maven-project


Q2160 Harun
  10:31 PM
Ekran


Ramazan - Instructor
  10:32 PM
http://3.235.177.197:8080/github-webhook/
:white_check_mark:
3

10:32
webhook eklendi.
:white_check_mark:
21

10:34
hello-app klasörü kopyalandı
:white_check_mark:
15



Q6202 - Huseyin Kartal
  10:34 PM
hocam klasor neredeydi git de


2 replies
Last reply today at 10:35 PMView thread


samuel
  10:35 PM
\clarusway-aws-devops-14\devops\hands-on\Jenkins\Session-2b-maven


Ramazan - Instructor
  10:36 PM
pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'mvn -f hello-app/pom.xml -B -DskipTests clean package'
            }
            post {
                success {
                    echo "Now Archiving the Artifacts....."
                    archiveArtifacts artifacts: '**/*.jar'
                }
            }
        }
        stage('Test') {
            steps {
                sh 'mvn -f hello-app/pom.xml test'
            }
            post {
                always {
                    junit 'hello-app/target/surefire-reports/*.xml'
                }
            }
        }
    }
}