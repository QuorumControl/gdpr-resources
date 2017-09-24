# GDPR Information

This information is not from lawyers and shouldn’t be considered legal advice. It is, rather, a representation or summary of what the GDPR means to businesses, as understood by the community.

## TLDR; What is the GDPR?

The GDPR is the General Data Privacy Regulation for the EU. It affects any company collecting personal information in the European Union (including foreign companies). It generally requires that you treat personal information with a high degree of respect and security. It also spells out data privacy and protection rights given to natural persons (people, not companies).

Non-compliance can result in loss of *4% of worldwide revenue (or €20mm) per infraction* (which can be per user). Non-compliance with this regulation is an existential threat to your organization.

## What is this repo?

It’s just a start! The goal of this repository is to provide as much easy to understand information as possible. It will initially focus on smaller businesses that need to be compliant and what they can do. This repo focuses on technology companies, but it is designed to be a growing resource. Please contribute! See How to Contribute. 

## More in-depth on GDPR

The “Key Changes Under GDPR” section of Microsoft’s website provide a decent overview of what’s required: https://www.microsoft.com/en-us/TrustCenter/Privacy/gdpr/default.aspx .

## What does it mean for smaller companies?

If you are a tech company (and don’t outsource your data processing) you are a “Processor” as defined by the regulation and will be required to do at least these things:

* Appoint a data protection officer (and let the state know about it)
* Secure personal data (more details to follow)
* Encryption
* Employee controls
* Private by design
* Make sure you have explicit permission to use whatever data you have (pre-checked checkboxes don’t count, the user must have an understanding
* Provide a way for users to opt-out and delete their data
* Breach notification - any breach that results in personal data loss (Names, emails, etc) requires notifying the state.

## Data Protection Officer

If you have more than 9 employees involved in automated data processing (read: 9 developers) you are required to have a data protection officer. Here is a good writeup of what the resonsibilities of that person are: https://iapp.org/news/a/top-10-operational-impacts-of-the-gdpr-part-2-the-mandatory-dpo/  . That position need-not be a dedicated position, however there is wording which prevents “conflict of interest” but what conflicts are not defined.

## Technical

Generally, you should treat your Personally Identifiable Information (PII) as highly sensitive data and limit use and access to it. Additionally, you should employ the most modern, up-to-date techniques to secure that data, including, but not limited to, encryption. 

The regulation is intentionally vague on what, explicitly, you need to do. Here are the three most relevant sections: https://gdpr-info.eu/art-32-gdpr/ ,https://gdpr-info.eu/art-25-gdpr/ , and https://gdpr-info.eu/art-35-gdpr/

The law is a little unclear as to how much protection you will be expected to provide. Generally I think you can envision a sliding scale where a storage of only email addresses might be OK providing decent security and a storage of financial and/or health information requiring a lot of protection. This recital should give you an idea of what the regulators are thinking of: https://gdpr-info.eu/recitals/no-75/

### General Guidelines

Follow normal infosec best practices. Including, but not limited to, keep your software up to date, don’t share passwords/accounts, encrypt your data at rest (including backups), limit what people have access, and constantly evaulate and monitor your security.

In talking to others, there seems to be some consensus on the following safeguards for protected personal information:

* If you can, don’t store it. If you don’t need PII, don’t keep it… it will be the easiest to protect
* Ideally keep your PII in a separate database. 
  * At least encrypt it at rest and access it over encrypted channels (most databases have a really easy way to do this now days).
* Limit access to PII to only applications and people that actually need access to perform their jobs.
* Keep audit logs of all access to PII.
* Understand what 3rd parties have access to your PII and explicitly sign contracts with them that guarantee they are also following the GDPR.

Some understand the law to go even farther with regards to data deletion. Users have the right to purge all their data from your system. This is generally a hard problem (given backups). 

## Links

https://www.microsoft.com/en-us/TrustCenter/Privacy/gdpr/default.aspx - Microsoft’s pretty complete analysis on your readiness
https://gdpr-info.eu - complete law (english), nicely formattted
https://gdpr-info.eu/art-32-gdpr/ - security of processing section
https://www.helpnetsecurity.com/2016/11/10/gdpr-privacy-study/ - what others are doing to prepare


## Similarities to other regulation.

### HIPAA
If you are familiar with HIPAA compliance in the US, you’ll find that this regulation “feels” very similar to that regulation. The GDPR has generally similar regulations that apply to all personal information and not just health information.

### German privacy law
Generally the GDPR is a strengthening and reiteration of existing german privacy law with some differences. However, if you’re already fully compliant with german privacy law, you are probably nearly compliant with GDPR.

## How to Contribute

Please fork and submit pull requests to this PR! I would love this to be a comprehensive resource for people trying to understand what the GDPR means to them. Please keep your wording simple. When you can, summarize and link-out to third party sources. If forking is too hard/confusing, please click “issues” at the top and describe the change you’d like to make. I’ll see if I can’t get your change in there for you!


