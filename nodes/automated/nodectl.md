---
title: nodectl
hide_table_of_contents: false
---

import DocsCard from '@components/global/DocsCard';
import DocsCards from '@components/global/DocsCards';

<head>
  <title>MainNet 2.0 Automation with nodectl</title>
  <meta
    name="description"
    content="MainNet 2.0 Automation"
  />
  <style>{`
    :root {
      --doc-item-container-width: 60rem;
    }
  `}
  </style>
</head>

:::danger IMPORTANT
The **manual instructions** to install a Node on MainNet 2.0 are for a **single Layer design**.  MainNet 2.0 will be requiring that you run both Layer0 and Layer1 as we perform Genesis.  

*This will change in the future*.
:::

:::success IMPORTANT
It is highly **recommended** that you use **nodectl** to install your Node!
:::

All Nodes will be required to run both the **Global Layer 0** and the **DAG State Channel Layer1**.

:::caution CAUTION
It is highly recommend to use the **latest** version of **NODECTL**!  It very possible that this documentation will fall behind and be a little out-of-date.  *Please correct the version in the url provided below, if necessary*.
:::

### DESCRIPTION

**nodectl** pronouced node "c" "t" "l", node-cuttle, or node control.

The purpose of this utility is to **make things easier** on you.  It obviates some of the technical aspects of running a Validator Node, so that anyone can do it!

### INSTALL YOUR NODE
Using `nodectl`

#### Step 1
Make sure you go through [Running a Node (Part 1)](../validator/install.md) and then go through the process of setting up your **VPS**.

:::danger
You will need to review the **required** specifications for MainNet 2.0 launch!  You can review them [here](../validator/specs.md)
:::

#### Step 2
Download the latest (this is important make sure you are at the latest version) of **nodectl**. (*Do not use any pre-releases*)
```
https://github.com/netmet1/constellation_nodectl/releases
```
Log into your VPS and download the latest release of **nodectl**.

The following commands will download the latest version, set the file's permissions and move it to the proper directory on your Linux VPS.

**x86_64** *(most common)*
```
sudo wget https://github.com/netmet1/constellation_nodectl/releases/download/v1.5.2/nodectl_x86_64 -P /usr/local/bin -O /usr/local/bin/nodectl; sudo chmod +x /usr/local/bin/nodectl
```

**arm_64**
```
sudo wget https://github.com/netmet1/constellation_nodectl/releases/download/v1.5.2/nodectl_arm64 -P /usr/local/bin -O /usr/local/bin/nodectl; sudo chmod +x /usr/local/bin/nodectl
```

:::note NOTE
After the initial download via a `wget` nodectl will warn you when a new versions are available.  at that time it will show you the proper command to issue to download the newest version
```
sudo nodectl upgrade_nodectl
```
:::

## INSTALL TESSELLATION LAYER0 and LAYER1

### STEP 1
```
sudo nodectl install
```

### STEP 2
The installation will take you through what information is needed by you, `step-by-step`.

### STEP 3
When your environment is requested, you should enter in `mainnet`

### STEP 4
Report your `nodeid` shown at the end of the process, to your administrators.

## OTHER IMPORTANT COMMANDS
show your nodeid
```
sudo nodectl nodeid
```
show your dag address
```
sudo nodectl dag
```
show your private key for import into your Stargazer wallet
```
sudo nodectl export_private_key
```