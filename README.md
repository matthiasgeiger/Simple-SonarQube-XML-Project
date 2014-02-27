Simple-SonarQube-XML-Project
========================

Simple project containing two BPMN-XML-Files to be analyzed using SonarQube XML Plugin: SimpleProcess.bpmn and SimpleProcess-Violation.bpmn which violates the normative BPMN XML schema definitions.

For a detailed description of the configuration and usage [see the blog post here](http://matthiasgeiger.wordpress.com/2014/02/26/sonarqube-tutorial-xml-plugin-setup-and-usage/ "SonarQube Tutorial: XML-Plugin – Setup and usage").

## Prerequisite
 - SonarQube Server must be installed and running
 - XML Plugin must be installed

## Configuration
To get feasable result some configuration steps must be performed:

- XML rules must be activated for the XML Quality Profiles
- For schema validation the "XML Schema validation" rule must be configured:
    - File pattern: e.g., `*.bpmn`
    - Schemas: `src/xsd/DC.xsd src/xsd/DI.xsd src/xsd/BPMNDI.xsd src/xsd/BPMN20-incl-Semantic.xsd`

## Analysis
To perform the analysis and add the project to the SonarQube server simply run a "sonar-runner" in the root directory of the project.

Project-specific configuration is stored in `sonar-project.properties` file.
