# ACR Assist

## Introduction

ACR Assist is a clinical decision support framework designed to provide structured clinical guidance to radiologists in a manner that allows this content to be incorporated naturally into the radiology workflow. The ACR Assist framework includes raw clinical content, an encoding scheme that allows this content to be consumed by commercial applications, and a communication framework that facilitates content delivery.

Radiology practice contains a large number of guidelines and algorithms for workup of specific clinical scenarios and findings. In order for these to be delivered within the context of a radiologist’s point-of-care (such as a PACS workstation or a voice recognition/report generation system), guidelines need to be specified in a structured format. The format developed and documented here serves as the interface between the creators of radiology reporting guidelines and the vendors of radiology reporting tools.

## Framework Schema

The schema is defined in [ACRAssist_xml_schema_beta2.0.rnc](https://github.com/acrscm/acr_assist_modules/blob/master/ACRAssist_xml_schema_beta2.0.rnc) using the RelaxNG Compact format ([specification](http://relaxng.org/compact-20021121.html); [tutorial](http://relaxng.org/compact-tutorial-20030326.html)).

The metadata schema defined in [Metadata.rnc] https://github.com/acrscm/acr_assist_modules/blob/master/Metadata.rnc

Briefly, the schema lays out the structure of guideline:
- **Metadata** section contains descriptive information about the guideline
- **Data Elements** section defines the various pieces of data used to characterize the clinical scenario and drive guidance and any logic
- **Rules** section defines the logic which can be run based on the input data elements to specify a guided output
- **End Points** section defines the actions to be taken based on the output of running the defined rules on the inputs given for a case.

## Sample Guideline

- **Hello Assist** is a simple guideline available at [Assist/Hello_Assist/Hello_Assist.xml](https://github.com/acrscm/acr_assist_modules/blob/master/Assist/Hello_Assist/Hello_Assist.xml).

- **Hello Rads** is another sample guideline is available at [Assist/Hello_Rads/Hello_Rads.xml](https://github.com/acrscm/acr_assist_modules/tree/master/Assist/Hello_Rads). The sample guideline (which is similar to the ACR's LI-RADS, but which is *not* an official ACR implementation of a LI-RADS tool) contains examples of common features.

## See Also

- [ACR Assist home page](https://www.acr.org/Practice-Management-Quality-Informatics/Informatics/Structured-Content)
- [Reference implementation for rendering and executing ACR Assist modules] (https://github.com/acrscm/acr_assist_simulator_control)
- [Try the simulator] (https://assist.acr.org/simulator/)



