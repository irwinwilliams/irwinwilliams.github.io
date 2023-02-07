---
title: "Provisioning some test storage accounts for class"
date: "2017-10-12"
categories: 
  - "cloud"
  - "teaching"
tags: 
  - "assignments"
  - "azure"
  - "bash"
  - "storage"
---

I wanted to create a few storage accounts for students in my class to complete an assignment featuring Event Sourcing and Material Views.

So, here's what I did.

Download/install the latest azure command line interface (cli). (While doing this, I realized I could have just used the cloud shell. I soldiered on with the dl)

Create a resource group to contain the accounts we'd need.

https://gist.github.com/irwinwilliams/df2a65b3ddc24b955f059188bd546125

Create the accounts and output the storage account keys The command to make a single storage account is pretty straightforward:

https://gist.github.com/irwinwilliams/6469286f83cf3d6a37f53d67687b4d52

But I wanted to also output the keys and display them on a single line. The command to get the keys after the account is created is this:

https://gist.github.com/irwinwilliams/63e998d4f9cbe054122a05cf492ea030

So, I used the jq program in bash to parse the json result and display both keys on a line. Thus, I created a script that would create the accounts and then output their storage account keys. This is the script that produced the accounts and keys:

https://gist.github.com/irwinwilliams/2884fabdc835b8a0c83dad9b7fef1961

Overall, the longest part of the exercise was dealing with the way the files were being saved in windows vs how they were being saved and read by bash. But the accounts were created and class can get on with assignment 2.
