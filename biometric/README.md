# Attacker Challenge: Face Recognition Evasion Track
<!-- vscode-markdown-toc -->
* [Overview](#overview)
    * [Challenge Dates](#challenge-dates)
    * [Rules / Terms](#rules-/-terms)
* [Submission Requirements](#requirements)
    * [Face Recognition evasion track submission requirements](#requirements)
* [Resources](#resources)

<!-- vscode-markdown-toc-config
	numbering=false
	autoSave=true
	/vscode-markdown-toc-config -->
<!-- /vscode-markdown-toc -->


## <a name='overview'></a>Overview

### <a name='challenge-dates'></a>Challenge Dates
Aug 12 - Sep 23, 2022 (AoE)

### <a name='rules-/-terms'></a>Rules / Terms
[https://mlsec.io/tos](https://mlsec.io/tos)

## Details

### Legend

An internet company wants to reinvent the experience for its website audience and use their faces instead of passwords. 

To implement this visionary idea, the company’s data scientists have built a model to recognize user faces for authentication. 

The internet isn't always safe, so their AI Red Team implemented some hardening techniques after adversarial testing. 

Before the official model rollout, the internet company requested some help from AI and cybersecurity communities.


### Model

The internet company has built an AI system with models that detect and recognize people's identities. 

Their system takes photos as an input, and if the face is detected, it's cropped and used for recognition. 

If confidence in the target identity is high enough, a user will be authenticated into their account.


### <a name='requirements'></a>Face recognition evasion track submission requirements
A valid face recognition evasion evasion submission consists of the following:
1. a ZIP file containing a maximum of 100 modified image samples (in `PNG` format) with the following naming convention: `<src>_<target>.png` (e.g. `1_2.png` where 1 is the original image, and 2 is the targeted celebrity for the ML model to detect)
2. partial ZIP uploads are okay, and can be used to "update" or "complete" a solution
3. uploads are not rate limited; but please do not overload the server
4. uploading ZIP files either via the API or the website results in all checks and database updates. Uploading the samples only to the API results only in ML results, but no database entry is created. The later is faster, but you have to upload via ZIP method to "store" the results. 


## <a name='resources'></a>Resources
For additional questions, the following resources are available:
* [API Description](https://mlsec.io/api_description/) for testing samples and uploading files
* [Join the Slack channel](https://join.slack.com/t/evademalwareml/shared_invite/zt-1e3pjht1s-h0H8omBFtZjZY1d5mKrokg) to interact with other contestants
* [Submit an issue](https://github.com/drhyrum/2022-machine-learning-security-evasion-competition/issues) 
