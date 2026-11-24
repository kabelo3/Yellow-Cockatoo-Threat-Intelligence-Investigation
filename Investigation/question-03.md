# Question 3: Malware Compilation Timestamp

## Question

Determining a malware sample's compilation timestamp can reveal insights into its development and deployment timeline. What compilation timestamp does VirusTotal show for this malware sample?

## Finding

**2020-09-24 18:26**

## Investigation Methodology

1. Opened [VirusTotal](https://www.virustotal.com/gui/home/search).
2. Searched for the malware sample using its SHA256 hash from `hash.txt`.
3. Navigated to the **Details** tab.
4. Located the **History** section.
5. Examined the **Creation Time** field.
6. Recorded the timestamp displayed by VirusTotal.

## Evidence

VirusTotal reports the following creation timestamp:

`2020-09-24 18:26`

## Tool Used

- VirusTotal

## Screenshot

Add the relevant screenshot below:

`![VirusTotal malware creation timestamp](../screenshots/question-03.png)`

## Security Relevance

Compilation timestamps can help analysts establish a possible development timeline for a malware sample and compare it with other known samples or threat activity.

However, timestamps should be treated as supporting evidence rather than definitive proof of when malware was developed or deployed. They can be manipulated or inaccurately reported.
