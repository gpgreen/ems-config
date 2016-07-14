# Usage instructions

1. Copy or update your ~/.m2/settings.xml with the settings.xml in this repository
2. For any Java maven project, use the mms-parent-pom.xml as the parent pom for your project
 * This contains all the distribution and repositories currently being used that correspond to the settings.xml file
 * Example for adding parent into pom

   	<parent>
		<groupId>gov.nasa.jpl</groupId>
		<artifactId>mms-parent-pom</artifactId>
		<version>1.0.0</version>
		<relativePath>config/mvn/mms-parent-pom.xml</relativePath>
	</parent>

