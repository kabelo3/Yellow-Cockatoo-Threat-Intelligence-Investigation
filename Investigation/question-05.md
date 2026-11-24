# Question 5: Identification of Dropped Malware Component

## Question

To completely eradicate the threat from GlobalTech Industries' systems, we need to identify all components dropped by the malware. What is the name of the `.dat` file that the malware dropped in the `AppData` folder?

## Finding

**`solarmarker.dat`**

## Investigation Methodology

1. Reviewed the threat intelligence information associated with the malware.
2. Located the relevant information under the **Zscaler** threat intelligence reference.
3. Examined the documented malware behaviour and associated dropped files.
4. Identified the `.dat` file reported in the Windows `AppData` folder.

## Evidence

The identified dropped file is:

`solarmarker.dat`

## Tool / Source Used

- Zscaler Threat Intelligence

## Screenshot

Add the relevant screenshot below:

`![SolarMarker dropped file identification](../screenshots/question-05.png)`

## Security Relevance

The Windows `AppData` directory is commonly used by legitimate applications to store application-specific data. Malware may also abuse this location to store payloads or supporting components.

Identifying dropped filenames helps incident responders develop detection searches and investigate potentially affected endpoints.

A filename alone is not sufficient to confirm malicious activity. Analysts should correlate it with its file path, hash, timestamps, and endpoint telemetry.
