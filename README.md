# java-word-count-beam
# java-word-count-beam

# Set up your Development Environment
Download and install the Java Development Kit (JDK) version 8. Verify that the JAVA_HOME environment variable is set and points to your JDK installation.
Download and install Apache Maven by following Maven’s installation guide for your specific operating system.
Optional: Install Gradle if you would like to convert your Maven project into Gradle.

# Instructions to be followed before execution
mvn archetype:generate `
 -D archetypeGroupId=org.apache.beam `
 -D archetypeArtifactId=beam-sdks-java-maven-archetypes-examples `
 -D archetypeVersion=2.36.0 `
 -D groupId=org.example `
 -D artifactId=word-count-beam `
 -D version="0.1" `
 -D package=org.apache.beam.examples `
 -D interactiveMode=false
 
 cd .\word-count-beam
 dir
 dir .\src\main\java\org\apache\beam\examples
 
 # Optional covertion from maven to gradle
 $ gradle init
 
 # How to build a maven project
 $ gradle build

 # Run wordcount using gradle
$ gradle clean execute -DmainClass=org.apache.beam.examples.WordCount \
    -Dexec.args="--inputFile=sample.txt --output=counts" -Pdirect-runner
    
 # Inspect the Results
    $ ls counts*
    
# Execution Commands:
mvn compile exec:java -D exec.mainClass=org.apache.beam.examples.WordCount `
 -D exec.args="--inputFile=sample.txt --output=counts" -P direct-runner
 
 
