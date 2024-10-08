---
layout: default
title: Data storage
parent: Guides
nav_order: 2
---

# Where to store your research data and code
{: .no_toc }
*Created by Neil Bramley on Sept 6, 2024, Last updated October 1st 2024*

**Too Long; Didn't Read:**

_The best thing to do:_ Keep your research data on your University DataStore network drive.

_The simplest way to do it:_ Just drag and drop it to your folder via File Explorer (Windows, M drive) or the Finder (Mac, Network/chss.datastore.ed.ac.uk/). More details for the curious, on setup and complicated cases below.

This is intended as a simple guide on storing research data while in PPLS. The primary goal is to ensure Principal Investigators, and other researchers responsible for data, maintain a "golden copy" of this data somewhere safe and secure, and preferably "in house", where it will not be lost, inappropriately leaked, sold, or monetised by third parties.  I also highlight various reasonable options for actively working on or sharing data and why other options are inappropriate.



<details open markdown="block">
  <summary>
    Table of contents
  </summary>
  {: .text-delta }
1. TOC
{:toc}
</details>

---




# In house options

## DataStore

The university has a network drive “DataStore”. This is the ideal place for PPLS staff and research students to archive a “golden copy” of their primary research data and code. At time of writing, each staff member gets a folder of their own with a default allocation of 500Gb and should contact the IT team if this is insufficient. Plans are in discussion to substantially increase the default allowance.

PPLS also creates & manages group spaces. So, if you run a lab, you can request a group space be created for you and this also allows the lab to pool allocations of group members. This is an equally good place to keep research data.

**How to get started?**

If your computer is managed by the university and runs Windows, DataStore should already appear as the “M:\\” drive.

If your computer is not managed by the university and runs Windows, [follow these instructions to add the drive](https://www.ed.ac.uk/information-services/computing/desktop-personal/connect-uni-file-storage/windows). You will have to be on campus wifi/ethernet or connected to the university [VPN](https://www.ed.ac.uk/information-services/computing/desktop-personal/vpn). Once it is added, you will be able to navigate (and create a shortcut) to your folder.

If your computer runs macOS you may need to set the drive up following [these instructions](https://www.ed.ac.uk/information-services/computing/desktop-personal/connect-uni-file-storage/macos). This is easy to do whether or not your machine is university managed (but the instructions differ). You will need to be in-network (on campus or on the VPN) to set up and to access the drive.

Find the path to your personal space [here](https://myadinfo.is.ed.ac.uk/MyInfo.aspx) while in network. For example, I (Neil Bramley) keep my archived research data in:  
> smb://chss.datastore.ed.ac.uk/chss/ppls/users/nbramley 

I maintain an original copy of data generated in my lab in:  
> smb://chss.datastore.ed.ac.uk/chss/ppls/groups/bramleyccslab.

If navigating through the DataStore network drive manually, you should see a folder “chss” (college of arts, humanities & social sciences), and within that there is a folder “/ppls”. Within "/ppls", there is a folder called “users” with a subfolder for every staff member’s unique username. Scroll to find yours and you should be able to add files to this folder (maybe create a shortcut to go straight there). 

To request access if you do not have a space already, or to add users to your lab group, fill in the form [here](https://www.ed.ac.uk/information-services/computing/desktop-personal/connect-uni-file-storage/request-datastore-access).

**The good**

It is bombproof. Data you put here is triple backed up, so very safe from loss, and accessible to the research team and appropriate administrators only, both on and off campus.

It is GDPR compliant. It is linked to Edinburgh’s [DataVault](https://datavault.ed.ac.uk/) for long term "cold storage". 

**The bad**

It is sluggish. At least on a Mac, it can take a minute to index the folders when you first navigate to the drive. It can take rather a long time for data to move on or off the drive. For these reasons, it is not the obvious place to read and write to data files while you are actively working on them. Think of it instead as the place to house a “golden copy” of your data so you never have to worry about losing it.

## OneDrive

**What is it?**

OneDrive is a core part of the University’s current Office 365 ecosystem. Access it from the 365 [Dashboard](https://www.office365.ed.ac.uk/) and if on Windows, also view it as a network drive similarly to DataStore. More information is available [here](https://www.ed.ac.uk/information-services/computing/comms-and-collab/office365/onedrive-for-business/how-to-access-onedrive-for-business). In principle, users can keep up to 1Tb of files in OneDrive and internal surveying shows that many researchers find OneDrive a practical place to keep data while they are actively working on it due to its integration with university email, Teams and SharePoint, etc. 

**However, OneDrive is not an appropriate place for keeping the ‘primary’ or ‘golden copy’ of your research data\!**

When researchers and students move on from Edinburgh university or change roles, their OneDrive folder is irrevocably deleted. There have been instances in PPLS of data loss due to the practice of keeping data solely on OneDrive. The potential for serious losses, and associated reputational embarrassment is high. **Please do not do this\!**

![](/assets/images/onedrive_sharepoint.png)


## DataShare

**What is it?**

[DataShare](https://datashare.ed.ac.uk/) is a University-managed service for hosting data so it is publicly available at the end of a link. Currently, you can host shareable files up to 20Gb through the interface (or up to 100Gb if you email). It is an in-house equivalent to hosting data on the Open Science Framework, or similar 3rd-party open research data repositories. You will be prompted to provide information about the dataset including links to any publications where it is used, but many are optional. After you upload, the central collection curation team will double check everything looks good before the link goes live.

**The good**

This is perhaps the most professional way to provide the general public with access to data collected at Edinburgh. The fact that it is an “in house” service allows for some confidence the link will continue to work for a very long time and never be monetised.

**The bad**

The web interface is a little buggy to use. I often I get a 503 error on first landing, which disappears when I refresh. I find the upload can take about 1 minute per Gb. You have to wait a couple of days for the curation team to check things before you get the live link.

## DataVault

While DataStore is appropriate for archiving data for completed projects, there is an additional service [DataVault](https://datavault.ed.ac.uk/) for “cold storage” of large chunks of data for the long term. This allows you to free up space in DataStore for data you are more likely to want to access. At the link above, you can create a DataVault and add folders from DataStore to it. They will then be deposited and become safe to delete from DataStore once you get the confirmation email. At time of writing Vaults for projects under 100Gb are free, and larger vaults may be funded from a prepaid slice purchased by PPLS or paid for by individuals with grant money. When the retention period expires (e.g. a default might be 10 years) the registered owner of the data, or if necessary, a delegated IT person, will be contacted about what should be done with it.

Note, if needed in the future, PPLS may implement a procedure for prompting users to move their largest or most inactive datasets to DataVault.

**The good**

Puts data somewhere safe and “out of the way” where it cannot be accidentally deleted and is not using up your lab's disk allocation.

**The bad**

I found the first time you create a vault, there are a couple of clunky steps that must be followed carefully. You must provide the DataStore path to the data in a slightly different format than how the path appears on your computer. You should also spend a little time documenting what you are storing so someone (even you) can make sense of it in the distant future. I found that the central Digital Research Services team are happy to help talk first time users through these steps on a Teams call.

## SharePoint

**What is it?**

SharePoint is a part of University of Edinburgh’s Office 365 ecosystem. It is a place for temporarily placing files that are being worked on collaboratively with a group of people such as a Team, Project or Department with real time syncing of the file across editors. For example, this is where an annual review form or a marking spreadsheet might be jointly edited by several researchers or staff members. **Even more so than OneDrive, SharePoint is not an appropriate place for keeping the ‘golden copy’ of research data\!**

## DataSync

[DataSync](https://www.ed.ac.uk/information-services/computing/desktop-personal/datasync) is the University’s Dropbox-like service for syncing files between machines. In this author’s view, it is too clunky and slow to be of practical use, but I have heard of at least one colleague who finds it useful.


# Third-party services

## Open Science Framework (OSF)

**What is it?**

The [OSF](https://osf.io/), or Open Science Framework, is currently a popular place for pre-registering experiments and analyses, hosting preprints of articles under consideration for publication, and also currently a widely used "repository" for providing open-source code and data associated with a publications or other research projects.

**The good**

Edinburgh currently has a [professional partnership with OSF](https://library.ed.ac.uk/research-support/research-data-service/during/open-research-tools/osf), making it a wholly appropriate place for sharing data and code (at least for now). You can sign in with your university credentials, there is integration with OneDrive. The site runs smoothly and is intuitive to use. You can make your projects public or private, embargo them until a certain date, or create anonymised links to repositories for including supplementary materials with submissions to journals and conferences requiring double-blinded reviewing. 

**The bad**

As a third party, your link might not be freely available in the long term. The company may go bust, start to monetise in ways that make it less of a sure bet than an “in-house” option.

## Github

**The good**

Github is great for sharing code. It is the industry standard for version control of large coding projects. 
If you share research data and code along with a paper it is good practice to use [Zenodo](https://zenodo.org/) to archive the "version of record" of the relevant repositor and provide a link to that. Otherwise the link you provide will point to a folder that may have changed by the time it is viewed, e.g. if you continue to work on the project.


**The bad**
You cannot keep much data in a Github repository. At time of writing there is a 100Gb limit per repository. Furthermore, the workflow of manually pushing, pulling, and merging changes to the remote copy is geared for working with code, not large data source files. Repositories are, by default, publicly accessible, so it is easy to expose passwords and private data if you keep project code there. Versioning code with Github requires a high level of tech-savvy, especially when there are multiple people contributing to, or “forking” the same repository. 


## Dropbox

Dropbox is a widely used service for syncing files across machines (and in the Cloud).  

**The good**: It can be a useful tool for allowing researchers working on several machines, or several academics keen to work locally on files in the same folder with near-instantaneous synchronisation. For this purpose it works far better than the University’s “in house” DataSync option.

**The bad**: Free-tier Dropbox is too small for most academic users and is not GDPR compliant.  Even with personal premium-tier membership, our understanding as of 2024 is that whenever one shares a research folder with a non-premium member (which is a common use case), the data is no longer GDPR compliant meaning you cannot legally store data containing identifiable information on Dropbox. **This makes Dropbox a poor tool for research data analysis if you have any sensitive or identifiable data.**  According to the [University’s guidance](https://www.ed.ac.uk/sites/default/files/atoms/files/quickguide\_02\_proof01\_0.pdf): *Don’t process research data on cloud services such as Dropbox without seeking advice. Cloud services not under contract to the University may not be stored on a UK or EU server, and may not be GDPR-compliant.*

## On Qualtrics or Testable

Common online data collection third-party services Qualtrics and Testable are currently under professional contracts with Edinburgh University and PPLS respectively. Their business models involve their holding a cloud copy of data you collect through them and encouraging you to draw it down directly from there for your analyses. **Tempting as it may be, this is not an appropriate or adequate solution for retaining the ‘golden copy’ of research data.** Please ensure you download a golden copy of any Qualtrics or Testable data and keep it in one of the places described above. It is commonplace to have difficulty reaching graduated students to access data linked to their Qualtrics or Testable accounts. Moreover, as a third-party service, when we end our contract with these companies we will lose free access to our own data, and risk its being sold or monetised.

## Your own integral or external hard drives

**Using your own drives is generally also not an adequate solution for retaining a “golden copy”, of research data.** Drives and laptops fail regularly in the short term and almost inevitably in the medium to long term.  Even if you have multiple external hard drives, this falls far short of the university’s network drive DataStore as a place for safekeeping data. If you do keep any sensitive data locally, according to the [University’s guidance](https://www.ed.ac.uk/sites/default/files/atoms/files/quickguide\_02\_proof01\_0.pdf): you also need to encrypt the drive *“Don’t keep copies of data with personally identifying information on portable media unless safeguards (such as encryption) are used.”* 

---

<!-- [Next: Preregistration Guide]({{ site.baseurl }}{% link docs/guides/preregistration.md %}) -->