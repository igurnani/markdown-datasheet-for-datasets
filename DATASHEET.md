# Datasheet: One Million Reddit Confessions

Author: Aaron Lin, Ishan Gurnani, Kyna Ha

Organization: UC Berkeley


## Motivation

*The questions in this section are primarily intended to encourage dataset creators to clearly articulate their reasons for creating the dataset and to promote transparency about funding interests.*

1. **For what purpose was the dataset created?** Was there a specific task in mind? Was there a specific gap that needed to be filled? Please provide a description.

The dataset was created to help figure out if a reddit confession could be classified as fake or not. While anonymity is an asset to many who wish to say something and get it off their chest, it can also be an outlet for internet trolls to make up stories in order to elicit some sort of response from readers and spread false information. Hence, this dataset aimed to try determining which of these stories are actually real and worth interacting with. 

2. **Who created this dataset (e.g. which team, research group) and on behalf of which entity (e.g. company, institution, organization)**?

Ishan Gurnani, Kyna Ha, and Aaron Lin for the UC Berkeley Class Info 159: Natural Language Processing

3. **What support was needed to make this dataset?** (e.g. who funded the creation of the dataset? If there is an associated grant, provide the name of the grantor and the grant name and number, or if it was supported by a company or government agency, give those details.)

There was no funding to help create this dataset. 

4. **Any other comments?**

	Not applicable


## Composition

*Dataset creators should read through the questions in this section prior to any data collection and then provide answers once collection is complete. Most of these questions are intended to provide dataset consumers with the information they need to make informed decisions about using the dataset for specific tasks. The answers to some of these questions reveal information about compliance with the EU’s General Data Protection Regulation (GDPR) or comparable regulations in other jurisdictions.*

1. **What do the instances that comprise the dataset represent (e.g. documents, photos, people, countries)?** Are there multiple types of instances (e.g. movies, users, and ratings; people and interactions between them; nodes and edges)? Please provide a description.

Each instance in the dataset represents one confession by a reddit user. The only instances we have are the confession and its label. 

2. **How many instances are there in total (of each type, if appropriate)?**

There are 1000 instances in total.

3. **Does the dataset contain all possible instances or is it a sample (not necessarily random) of instances from a larger set?** If the dataset is a sample, then what is the larger set? Is the sample representative of the larger set (e.g. geographic coverage)? If so, please describe how this representativeness was validated/verified. If it is not representative of the larger set, please describe why not (e.g. to cover a more diverse range of instances, because instances were withheld or unavailable).

This is a sample taken from the dataset one million reddit confessions. The dataset was randomly chosen from this data so we hope it is representative of the larger set. 

4. **What data does each instance consist of?** "Raw" data (e.g. unprocessed text or images) or features? In either case, please provide a description.

The data consists of unprocessed text. It starts off with the title of the post, then an [end title] marking to indicate the rest of the text is the body of the confession. 

5. **Is there a label or target associated with each instance?** If so, please provide a description.

The labels for each instance are either real or fake depending on the way that we classified it. 

6. **Is any information missing from individual instances?** If so, please provide a description, explaining why this information is missing (e.g. because it was unavailable). This does not include intentionally removed information, but might include, e.g. redacted text.

There is no data missing from individual instances since before we sampled the data, we dropped all data that had text labeled [removed] or [deleted]

7. **Are relationships between individual instances made explicit (e.g. users' movie ratings, social network links)?** If so, please describe how these relationships are made explicit.

There are no relationships between individual instances. 

8. **Are there recommended data splits (e.g. training, development/validation, testing)?** If so, please provide a description of these splits, explaining the rationale behind them.

We have no recommendations for data splits. 

9. **Are there any errors, sources of noise, or redundancies in the dataset?** If so, please provide a description.

There are no errors, sources of noise, or redundancies as all instances are individual and unrelated to the others, and were only sampled from confessions that were not redacted. 

10. **Is the dataset self-contained, or does it link to or otherwise rely on external resources (e.g. websites, tweets, other datasets)?** If it links to or relies on external resources, a) are there guarantees that they will exist, and remain constant, over time; b) are there official archival versions of the complete dataset (i.e., including the external resources as they existed at the time the dataset was created); c) are there any restrictions (e.g. licenses, fees) associated with any of the external resources that might apply to a future user? Please provide descriptions of all external resources and any restrictions associated with them, as well as links or other access points, as appropriate.

The dataset is self contained. 

11. **Does the dataset contain data that might be considered confidential (e.g. data that is protected by legal privilege or by doctor-patient confidentiality, data that includes the content of individuals' non-public communications)?** If so, please provide a description.

There is no confidentiality breach since all of the confessions are anonymous. 

12. **Does the dataset contain data that, if viewed directly, might be offensive, insulting, threatening, or might otherwise cause anxiety?** If so, please describe why.

Yes it does. Many of the confessions deal with mental health issues, self-harm, or things of sexual nature which make upset many. 

13. **Does the dataset relate to people?** If not, you may skip the remaining questions in this section.

It does relate to people as the confessions are all written by people. 

14. **Does the dataset identify any subpopulations (e.g. by age, gender)?** If so, please describe how these subpopulations are identified and provide a description of their respective distributions within the dataset.

The dataset does not identify subpopulations. 

15. **Is it possible to identify individuals (i.e., one or more natural persons), either directly or indirectly (i.e., in combination with other data) from the dataset?** If so, please describe how.

It is not possible since we dropped the username of the author from the dataset and the confessions are anonymous. 

16. **Does the dataset contain data that might be considered sensitive in any way (e.g. data that reveals racial or ethnic origins, sexual orientations, religious beliefs, political opinions or union memberships, or locations; financial or health data; biometric or genetic data; forms of government identification, such as social security numbers; criminal history)?** If so, please provide a description.

Yes, as many people post confessions related to their mental health, race, sex, religion, and political beliefs. However it does not do so in an incriminating way where these things are explicitly listed. Rather, people describe this in the text itself. 

17. **Any other comments?**

Not applicable.

## Collection

*As with the previous section, dataset creators should read through these questions prior to any data collection to flag potential issues and then provide answers once collection is complete. In addition to the goals of the prior section, the answers to questions here may provide information that allow others to reconstruct the dataset without access to it.*

1. **How was the data associated with each instance acquired?** Was the data directly observable (e.g. raw text, movie ratings), reported by subjects (e.g. survey responses), or indirectly inferred/derived from other data (e.g. part-of-speech tags, model-based guesses for age or language)? If data was reported by subjects or indirectly inferred/derived from other data, was the data validated/verified? If so, please describe how.

The data was directly observable from reddit confessions pages. 

2. **What mechanisms or procedures were used to collect the data (e.g. hardware apparatus or sensor, manual human curation, software program, software API)?** How were these mechanisms or procedures validated?

The data was downloaded from kaggle, and originally from the website socialgrep. 

3. **If the dataset is a sample from a larger set, what was the sampling strategy (e.g. deterministic, probabilistic with specific sampling probabilities)?**

We used a simple random sampling technique to sample our dataset from the larger data. 

4. **Who was involved in the data collection process (e.g. students, crowdworkers, contractors) and how were they compensated (e.g. how much were crowdworkers paid)?**

The data collection was students and we were given a grade. 

5. **Over what timeframe was the data collected?** Does this timeframe match the creation timeframe of the data associated with the instances (e.g. recent crawl of old news articles)? If not, please describe the timeframe in which the data associated with the instances was created. Finally, list when the dataset was first published.

The timeframe of the data is confessions before September 2021, and published in September. 

7. **Were any ethical review processes conducted (e.g. by an institutional review board)?** If so, please provide a description of these review processes, including the outcomes, as well as a link or other access point to any supporting documentation.

Not applicable. 

8. **Does the dataset relate to people?** If not, you may skip the remainder of the questions in this section.

Yes. 

9. **Did you collect the data from the individuals in question directly, or obtain it via third parties or other sources (e.g. websites)?**

The data was collected from reddit, a third party. 

10. **Were the individuals in question notified about the data collection?** If so, please describe (or show with screenshots or other information) how notice was provided, and provide a link or other access point to, or otherwise reproduce, the exact language of the notification itself.

The individuals do not know that their confessions were collected. 

11. **Did the individuals in question consent to the collection and use of their data?** If so, please describe (or show with screenshots or other information) how consent was requested and provided, and provide a link or other access point to, or otherwise reproduce, the exact language to which the individuals consented.

They did not consent to the use of their confessions in the data. 

12. **If consent was obtained, were the consenting individuals provided with a mechanism to revoke their consent in the future or for certain uses?** If so, please provide a description, as well as a link or other access point to the mechanism (if appropriate).

Not applicable. 

13. **Has an analysis of the potential impact of the dataset and its use on data subjects (e.g. a data protection impact analysis) been conducted?** If so, please provide a description of this analysis, including the outcomes, as well as a link or other access point to any supporting documentation.

Not applicable. 

14. **Any other comments?**

Not applicable. 


## Preprocessing / Cleaning / Labeling

*Dataset creators should read through these questions prior to any pre-processing, cleaning, or labeling and then provide answers once these tasks are complete. The questions in this section are intended to provide dataset consumers with the information they need to determine whether the “raw” data has been processed in ways that are compatible with their chosen tasks. For example, text that has been converted into a “bag-of-words” is not suitable for tasks involving word order.*

1. **Was any preprocessing/cleaning/labeling of the data done (e.g. discretization or bucketing, tokenization, part-of-speech tagging, SIFT feature extraction, removal of instances, processing of missing values)?** If so, please provide a description. If not, you may skip the remainder of the questions in this section.

We removed all instances of the data where the text was labeled as [removed] or [redacted], which was about half of the data. 

2. **Was the "raw" data saved in addition to the preprocessed/cleaned/labeled data (e.g. to support unanticipated future uses)?** If so, please provide a link or other access point to the "raw" data.

Not applicable. 

3. **Is the software used to preprocess/clean/label the instances available?** If so, please provide a link or other access point.

Not applicable. 

4. **Any other comments?**

Not applicable. 


## Uses

*These questions are intended to encourage dataset creators to reflect on the tasks  for  which  the  dataset  should  and  should  not  be  used.  By  explicitly highlighting these tasks, dataset creators can help dataset consumers to make informed decisions, thereby avoiding potential risks or harms.*

1. **Has the dataset been used for any tasks already?** If so, please provide a description.

The dataset has not been used for any task yet. 

2. **Is there a repository that links to any or all papers or systems that use the dataset?** If so, please provide a link or other access point.

There is no repository of papers that use the dataset. 

3. **What (other) tasks could the dataset be used for?**

The dataset can only be used to classify reddit confessions as real or fake. Any other applications would be met with many errors and inconsistencies. 

4. **Is there anything about the composition of the dataset or the way it was collected and preprocessed/cleaned/labeled that might impact future uses?** For example, is there anything that a future user might need to know to avoid uses that could result in unfair treatment of individuals or groups (e.g. stereotyping, quality of service issues) or other undesirable harms (e.g. financial harms, legal risks) If so, please provide a description. Is there anything a future user could do to mitigate these undesirable harms?

There is nothing about the composition of the dataset that might impact future uses. 

5. **Are there tasks for which the dataset should not be used?** If so, please provide a description.

Any task that is not classifying a reddit confession as real or fake. 

6. **Any other comments?**

Not applicable. 


## Distribution

*Dataset creators should provide answers to these questions prior to distributing the dataset either internally within the entity on behalf of which the dataset was created or externally to third parties.*

1. **Will the dataset be distributed to third parties outside of the entity (e.g. company, institution, organization) on behalf of which the dataset was created?** If so, please provide a description.

The dataset will be made available to the public. 

2. **How will the dataset will be distributed (e.g. tarball on website, API, GitHub)?** Does the dataset have a digital object identifier (DOI)?

The dataset will be distributed by being posted on GitHub. 

3. **When will the dataset be distributed?**

The dataset will be distributed in the next month. 

4. **Will the dataset be distributed under a copyright or other intellectual property (IP) license, and/or under applicable terms of use (ToU)?** If so, please describe this license and/or ToU, and provide a link or other access point to, or otherwise reproduce, any relevant licensing terms or ToU, as well as any fees associated with these restrictions.

Not applicable. 

5. **Have any third parties imposed IP-based or other restrictions on the data associated with the instances?** If so, please describe these restrictions, and provide a link or other access point to, or otherwise reproduce, any relevant licensing terms, as well as any fees associated with these restrictions.

Not applicable. 

6. **Do any export controls or other regulatory restrictions apply to the dataset or to individual instances?** If so, please describe these restrictions, and provide a link or other access point to, or otherwise reproduce, any supporting documentation.

Not applicable. 

7. **Any other comments?**

Not applicable. 


## Maintenance

*As with the previous section, dataset creators should provide answers to these questions prior to distributing the dataset. These questions are intended to encourage dataset creators to plan for dataset maintenance and communicate this plan with dataset consumers.*

1. **Who is supporting/hosting/maintaining the dataset?**

The dataset authors, Aaron Lin, Ishan Gurnani, and Kyna Ha are hosting the dataset. 

2. **How can the owner/curator/manager of the dataset be contacted (e.g. email address)?**

aarlin@berkeley.edu
kyha@berkeley.edu
igurnani@berkeley.edu 

3. **Is there an erratum?** If so, please provide a link or other access point.

There is no erratum.

4. **Will the dataset be updated (e.g. to correct labeling errors, add new instances, delete instances)?** If so, please describe how often, by whom, and how updates will be communicated to users (e.g. mailing list, GitHub)?

The dataset will not be updated. 

5. **If the dataset relates to people, are there applicable limits on the retention of the data associated with the instances (e.g. were individuals in question told that their data would be retained for a fixed period of time and then deleted)?** If so, please describe these limits and explain how they will be enforced.

No, there are no limits on the retention of the data. 

6. **Will older versions of the dataset continue to be supported/hosted/maintained?** If so, please describe how. If not, please describe how its obsolescence will be communicated to users.

Not applicable. This will be the only version of the dataset. 

7. **If others want to extend/augment/build on/contribute to the dataset, is there a mechanism for them to do so?** If so, please provide a description. Will these contributions be validated/verified? If so, please describe how. If not, why not? Is there a process for communicating/distributing these contributions to other users? If so, please provide a description.

Others can resample from the one million reddit confessions as we did and manually create labels for each instance using the guidelines we created. 

8. **Any other comments?**

Not applicable. 
