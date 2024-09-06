---
layout: default
title: Data storage
parent: Guides
nav_order: 2
---

# Where to store your data and code
{: .no_toc }

<details open markdown="block">
  <summary>
    Table of contents
  </summary>
  {: .text-delta }
1. TOC
{:toc}
</details>

---

# In house services

## DataStore

The university has a network drive “DataStore”. This is the ideal place for PPLS staff and research students to archive a “golden copy” of their primary research data and code.

At time of writing, staff members get a folder of their own with a default allocation of 500Gb and should contact the IT team if this is insufficient for their needs.

PPLS also creates & manages group spaces, so If you run a lab, you can request a group space be created for you and this allows you to pool allocations of group members and is an equally good place to keep research data.

For example, I (Neil Bramley) keep my archived research data in:  
> smb://chss.datastore.ed.ac.uk/chss/ppls/users/nbramley 

I maintain an original copy of data generated in my lab in:  
> smb://chss.datastore.ed.ac.uk/chss/ppls/groups/bramleyccslab.

**How to get started?**

Find the path to your personal space [here](https://myadinfo.is.ed.ac.uk/MyInfo.aspx) – For this to work, you have to be connected to campus wifi or ethernet or to the university’s [VPN](https://www.ed.ac.uk/information-services/computing/desktop-personal/vpn).

If your computer is managed by the university and runs Windows, DataStore should already appear as the “M:\\” drive.

If your computer is not managed by the university and runs Windows [follow these instructions to add the drive](https://www.ed.ac.uk/information-services/computing/desktop-personal/connect-uni-file-storage/windows). You will have to be on campus wifi/ethernet or connected to the university [VPN](https://www.ed.ac.uk/information-services/computing/desktop-personal/vpn). Once it is added, you will be able to navigate to, and create a shortcut to,  your folder as above.

If your computer runs macOS you may need to set the drive up following [these instructions](https://www.ed.ac.uk/information-services/computing/desktop-personal/connect-uni-file-storage/macos). 

This is easy to do whether or not the computer is university managed (but the instructions differ). In either case you will need to be in-network (on campus or on the VPN).

If navigating through the DataStore network drive manually, you should see a folder “chss” (college of arts, humanities & social sciences), and within that there is a folder “/ppls”. Within ppls, there is a folder called “users” with a subfolder for every staff member’s unique username. Scroll to find yours and you should be able to add files to this folder (maybe create a shortcut to go straight there). 

Note (on my mac) I find the outer folders can take several minutes to index the first time you navigate through them so be patient and it should speed up once it has indexed.

To request access if you do not have a space already. Or to add users to your lab group, fill in the form [here](https://www.ed.ac.uk/information-services/computing/desktop-personal/connect-uni-file-storage/request-datastore-access).

**The good**

It’s bombproof: Data you put here is triple backed up, so very safe from loss accessible both on and off campus

It is linked with to Edinburgh’s [DataVault](https://datavault.ed.ac.uk/) for long term cold storage. 

**The bad**

It is sluggish. At least on a Mac, it can take a minute to index the folders when you first navigate to the drive. It can take rather a long time for data to move on or off the drive. For these reasons, it is not the obvious place to read and write data while you are actively working on it. Think of it instead as the place to house golden copy data so you never have to worry about losing it.

## OneDrive

**What is it?**

Onedrive is a core part of the University’s current Office 365 ecosystem. Access it from the 365 [Dashboard](https://www.office365.ed.ac.uk/) and view it as a network drive similarly to DataStore. [This](https://www.ed.ac.uk/information-services/computing/comms-and-collab/office365/onedrive-for-business/how-to-access-onedrive-for-business) is a useful link if you have any difficulty with this. In principle, users can keep up to 1Tb of files in OneDrive and many researchers find it a practical place for keeping data while they are actively working on it due to its integration with university email, Teams and SharePoint, etc. 

![](/assets/images/onedrive_sharepoint.png)

**However, OneDrive is not an appropriate place for keeping the ‘primary’ or  ‘golden copy’ of research data\!** When researchers move on from the university their OneDrive gets deleted. There have been instances of data loss through the practice of keeping data on OneDrive. Please do not do this\!


## DataShare

**What is it?**

[DataShare](https://datashare.ed.ac.uk/) is a service for hosting data so it is publicly available at the end of a link. Currently, you can host sharable files up to 20Gb through the interface (or up to 100Gb by emailing them). It is like an in-house equivalent to hosting data on the Open Science Framework, or other 3rd party data repositories. You will be prompted to provide information about the dataset including links to any publications where it is used but many are optional.

**The good**

This is perhaps the most professional way to provide the general public with access to data collected at Edinburgh. The fact that it is an “in house” service allows for more confidence the link will continue to work for a very long time and never be monetised.

**The bad**

The web interface is a little buggy to use and upload can take a few minutes.

## DataVault

While DataStore is appropriate for archiving data for completed projects, there is an additional service [DataVault](https://datavault.ed.ac.uk/) for “cold storage” of larger chunks of data for the long term, allowing you to free up space in DataStore. At the link above you can create a DataVault and add folders from DataStore to it. They will then be deposited and become safe to delete from DataStore. At time of writing Vaults for projects under 100Gb are free, and larger vaults may be funded from a prepaid slice purchased by PPLS or paid for by individuals with grant money. When the retention period expires (e.g. in 10 years)  the registered owner of the data, or a delegated IT person will be contacted about what should be done with it.

Note, in future, moving large pieces of PPLS-owned data that have not been needed in a long time to DataVault may be coordinated partly by our IT team.

**The good**

Puts data somewhere safe and “out of the way” where it cannot be accidentally deleted and is not using up your disk allocation.

**The bad**

At time of writing, I found the first time you create a vault, there are a couple of clunky steps that must be followed carefully: e.g. you must provide the DataStore path to the data in a slightly different format than the path on your computer. You should also spend a little time documenting what you are storing so someone can make sense of it in the distant future. The central Digital Research Services team are happy to help talk first time users through these steps on a Teams call.

## Sharepoint

**What is it?**

Sharepoint is a part of University of Edinburgh’s Office 365 ecosystem. It is a place for temporarily placing files that need to be shared or used in collaboration with a group of people such as a Team, Project or Department. E.g. this is where an annual review form or a marking spreadsheet might be jointly edited by several researchers or staff members. **Like OneDrive, Sharepoint is not an appropriate place for keeping the ‘golden copy’ of research data\!**

## DataSync

[DataSync](https://www.ed.ac.uk/information-services/computing/desktop-personal/datasync) is the University’s Dropbox-like service for syncing files between machines. Unfortunately in this author’s view, it is too buggy and slow to be of much practical use, but any positive experiences using DataSync would be welcome.


# Third party services

## Open Science Framework (OSF)

**What is it?**

The [OSF](https://osf.io/), or Open Science Framework, is a popular place for pre-registering experiments and analyses, hosting preprints of articles under consideration for publication and also a helpful palace for providing code and data associated with a project.

**The good**

Edinburgh currently has a [professional partnership with OSF](https://library.ed.ac.uk/research-support/research-data-service/during/open-research-tools/osf), making it a great and appropriate place for sharing data and code. You can sign in with your University credentials, there is integration with OneDrive. The site runs smoothly and is intuitive to use. You can make your projects public or private, embargo them until a certain date, or create anonymised links to repositories for including supplementary materials with submissions to journals and conferences requiring double blinded reviewing. 

**The bad**

As a third party your link might not be freely available in the long term. The company may go bust or start to monetise in ways that make it a little less of a sure bet than an “in house” option.

## Github

Github is great for code but you can’t really keep much data in a github repository. At time of writing there was a 100Gb limit on repository sizes, and the workflow of pushing and pulling changes to the cloud is not really geared for working with large files. Repositories are, by default, publically accessible, so it is easy to expose passwords and private data if you keep project code there. Versioning code with github requires a fairly high level of tech-savvy, especially when there are multiple people contributing to, or “forking” the same repository. However it is the industry standard for version control of large coding projects.

If you share research data and code along with a paper it is good practice to to use [Zenodo](https://zenodo.org/) to archive a version of record, of your repository, as otherwise the link you provide will point to a folder that may have changed by the time it is viewed.

## Dropbox

Dropbox is a widely used service for syncing files across machines (and in the Cloud).  

**The good**: It can be a useful tool for allowing researchers working on several machines, or several academics keen to work locally on files in the same folder with near-instantaneous synchronisation. For this purpose it works far better than the University’s “in house” DataSync option.

**The bad**: Free-tier Dropbox is too small for most academic users and is not GDPR compliant.  Even with personal premium-tier membership, our understanding as of 2024 is that whenever one shares a research folder with a non-premium member (which is a common use case), the data is no longer GDPR compliant meaning you cannot legally store data containing identifiable information on Dropbox, **making it a poor tool for research data analysis if you have any sensitive or identifiable data.**  According to the [University’s guidance](https://www.ed.ac.uk/sites/default/files/atoms/files/quickguide\_02\_proof01\_0.pdf): *Don’t process research data on cloud services such as Dropbox without seeking advice. Cloud services not under contract to the University may not be stored on a UK or EU server, and may not be GDPR-compliant.*


## Your own laptop or your own external hard drive or USB drive

According to the [University’s guidance](https://www.ed.ac.uk/sites/default/files/atoms/files/quickguide\_02\_proof01\_0.pdf): You should encrypt the drive *“Don’t keep copies of data with personally identifying information on portable media unless safeguards (such as encryption) are used.”* **Using your own drives is generally also not an adequate solution for retaining a “golden copy”, “original” or “only copy” of research data.** Drives and laptops fail regularly so fall far short of the university’s triple-backed up network drive as a place for safekeeping data.

---

<!-- [Next: Preregistration Guide]({{ site.baseurl }}{% link docs/guides/preregistration.md %}) -->