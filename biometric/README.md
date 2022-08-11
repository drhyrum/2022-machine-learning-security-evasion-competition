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

### Story

An internet company wants to reinvent the experience for its website audience and use their faces instead of passwords. 

To implement this visionary idea, the company’s data scientists have built a model to recognize user faces for authentication. 

The internet isn't always safe, so their AI Red Team implemented some hardening techniques after adversarial testing. 

Before the official model rollout, the internet company requested some help from AI and cybersecurity communities.


### Model

The internet company has built an AI system with models that detect and recognize people's identities. 

Their system takes photos as an input, and if the face is detected, it's cropped and used for recognition. 

If confidence in the target identity is high enough, a user will be authenticated into their account.


### Dataset

The data for facial recognition evaluation includes photos of 10 selected website users. 

Images are provided in a PNG format with filenames ranging from 0-9 representing user IDs.


### Challenge

Contest participants compete in crafting efficient evasion and impersonation attacks against the facial recognition model. 

The goal is to modify user photos to evade an original identity and impersonate a target identity while preserving image quality.


### Submission

It’s required to turn each identity `source` into every other identity `target` with a total of 90 attack pairs. 

Every `source_target` submission receives metrics indicating attack quality and image quality.


### Judging

Winners are defined based on the best metrics from all of submitted 90 attack pairs. 

The main competition metric is Confidence with Stealthiness used as the tie-breaker metric.


### Metrics

**Confidence**. Range (0,1), high is good. Shows probability of an adversarial image to a target class.

**Stealthiness**. Range (0,1), high is good. Shows structural similarity of an adversarial image to a source image.

**Success**. Range (True, False), True is good. Shows if an adversarial image is recognized as a target class successfully AND if an adversarial image preserves original image quality defined by `stealthiness>=0.5`.



### Advice

#### API usage
* Develop and debug your adversarial examples with API for single image testing (results are not stored in the MLSEC system)
* Submit and register your adversarial examples with API for ZIP file manipulation (results are stored in the MLSEC system)


#### API responses

* Valid submission responses look like `{"confidence": 0.823142, "stealthiness": 0.56949, "success": true}`

* Invalid submission responses look like `{ "confidence": 0.0, "stealthiness": 0.0, "success": false }`

Common submission errors:
* Adversarial image is linked to invalid source or target IDs
* Adversarial image doesn’t contain a face as detected by the model

### <a name='requirements'></a>Submission requirements

A valid face recognition evasion submission consists of the following:

* ZIP archive submissions can be full or partial with 1 to 90 image files included
* Image files must be in `PNG` format and follow the naming convention: `<source_id>_<target_id>.png` such as `0_1.png`
* Image files with the same names will be analyzed only once unless their checksums are different
* ZIP archive submissions are not limited and can be used to update or complete the solution
* ZIP archive submissions are processed in batches according to a server schedule
* ZIP archive submissions can be encrypted with the password `infected`


## <a name='resources'></a>Resources
For additional questions, the following resources are available:
* [API Description](https://mlsec.io/api_description/) for testing samples and uploading files
* [Join the Slack channel](https://join.slack.com/t/evademalwareml/shared_invite/zt-1e3pjht1s-h0H8omBFtZjZY1d5mKrokg) to interact with other contestants
* [Submit an issue](https://github.com/drhyrum/2022-machine-learning-security-evasion-competition/issues) 
