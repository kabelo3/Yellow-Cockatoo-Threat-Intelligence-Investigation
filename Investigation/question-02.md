# Question 2: Malware Filename Identification

## Question

As part of our incident response, knowing the malware's common filenames can help us scan other workstations for potential infection. What is the common filename associated with this malware?

## Finding

**`111bc461-1ca8-43c6-97ed-911e0e69fdf8.dll`**

## Investigation Methodology

1. Opened [VirusTotal](https://www.virustotal.com/gui/home/search).
2. Copied the SHA256 hash from the provided `hash.txt` file.
3. Pasted the hash into the VirusTotal search field.
4. Reviewed the file's analysis results.
5. Identified the associated filename displayed in the file information.

## Evidence

VirusTotal displayed the following filename associated with the submitted SHA256 hash:

`111bc461-1ca8-43c6-97ed-911e0e69fdf8.dll`

## Tool Used

- VirusTotal

## Screenshot

Add the relevant screenshot below:

`![VirusTotal malware filename](../screenshots/question-02.png)`

## Security Relevance

Malware filenames can serve as useful indicators during incident response. Security teams can use identified filenames to support endpoint investigations and search for potentially related files across other workstations.

However, filenames alone are not reliable proof of infection because malicious files can be renamed. They should be correlated with hashes, file paths, endpoint telemetry, and other indicators of compromise.
