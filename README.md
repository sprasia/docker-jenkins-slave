# Jenkins JNLP Agent Docker image

This is an image for [Jenkins](https://jenkins.io) agent (FKA "slave") using JNLP to establish connection.
This agent is powered by the [Jenkins Remoting library](https://github.com/jenkinsci/remoting).

See [Jenkins Distributed builds](https://wiki.jenkins-ci.org/display/JENKINS/Distributed+builds) for more info.

## Running

To run a Docker container with [Work Directory](https://github.com/jenkinsci/remoting/blob/master/docs/workDir.md):

    docker run -e "JENKINS_JNLP_URL=https://jenkins-server:port/computer/agent-name/slave-agent" -e "JENKINS_AGENT_WORKDIR=/home/jenkins/agent" sprasia/jenkins-slave
