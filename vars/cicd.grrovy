def newGit(repo)
{
    git "https://github.com/vidyasrees/${repo}.git"
}
def newMaven()
{
    sh "mvn package"
}
def newDeploy(jobname,ip,context)
{
    sh "scp /var/lib/jenkins/workspace/${jobname}/webapp/target/webapp.war ubuntu@${ip}:/var/lib/tomcat10/webapps/${context}.war"
}
def runSelenium(jobname)
{
     sh "java -jar /var/lib/jenkins/workspace/${jobname}/testing.jar"
}
