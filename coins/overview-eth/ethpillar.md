---
description: >-
  Empowered, inspired, home staker. Free. Open source. Public goods for
  Ethereum.
---

# 🛡️ EthPillar: one-liner setup tool and node management TUI

## :new: What is EthPillar?

:smile: **Friendly Node Installer**: No node yet? Helps you installs a Ethereum node (Nimbus+Nethermind) stack in just minutes. MEVboost included.

:floppy\_disk: **Ease of use**: No more remembering CLI commands required. Access common node operations via a simple text user interface (TUI).

:owl: **Fast Updates**: Quickly find and download the latest consensus/execution release. Less downtime!

:tada:**Compatibility**: Behind the scenes, node commands and file structure are identical to V2 staking setups.&#x20;

{% hint style="warning" %}
Already a running a Validator? EthPillar is compatible with [a Coincashew V2 Staking Setup.](https://www.coincashew.com/coins/overview-eth/guide-or-how-to-setup-a-validator-on-eth2-mainnet)&#x20;
{% endhint %}

<figure><img src="../../.gitbook/assets/ethpillar.png" alt=""><figcaption><p>EthPillar Main Menu</p></figcaption></figure>

## Prerequisites

* [Review how staking works and the hardware requirements](guide-or-how-to-setup-a-validator-on-eth2-mainnet/part-i-installation/prerequisites.md)
* An [Ubuntu](guide-or-how-to-setup-a-validator-on-eth2-mainnet/part-i-installation/prerequisites.md#setup-ubuntu) installation. Tested working with v22.04 LTS.

## Option 1: Automated One-Liner Install

Simply copy and paste the command into your terminal.

Open source source code available here: [https://github.com/coincashew/EthPillar](https://github.com/coincashew/EthPillar)

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/coincashew/ethpillar/master/install.sh)"
```

## Option 2: Manual Install

**Install updates and packages:**

```bash
sudo apt-get update && sudo apt-get install git curl ccze
```

**Clone the ethpillar repo and install:**

```bash
mkdir -p ~/git/ethpillar
git clone https://github.com/coincashew/ethpillar.git ~/git/ethpillar
sudo ln -s ~/git/ethpillar/ethpillar.sh /usr/local/bin/ethpillar
```

#### Run ethpillar:

```bash
ethpillar
```

## :tada:Next Steps

{% hint style="success" %}
Congrats on installing a EthPillar, making nodes and home staking easier!
{% endhint %}

<details>

<summary>Additional step for new Node operators</summary>

Step 1: Configure your network, port forwarding and firewall. From the main guide, [click here for detailed network configuration](guide-or-how-to-setup-a-validator-on-eth2-mainnet/part-i-installation/step-2-configuring-node.md#network-configuration).

* Involves setting UFW defaults, opening SSH port, allowing consensus/execution p2p port traffic, enabling the UFW firewall, configuring port forwarding and installing fail2ban.

</details>

<details>

<summary>Additional steps for new Validators</summary>

**Step 1: Setup Validator Keys**

* Familarize yourself with the main guide's section on [setting up your validator keys.](guide-or-how-to-setup-a-validator-on-eth2-mainnet/part-i-installation/step-5-installing-validator/setting-up-validator-keys.md)
* When ready to generate your keys, go to **EthPillar > Validator Client > Generate / Import Validator Keys**

**Step 2: Upload deposit\_data.json to Launchpad**

* To begin staking on Ethereum as a validator, you need to submit to the Launchpad your  deposit\_data.json file, which includes crucial withdrawal address details, and pay the required deposit of 32ETH per validator.

**Step 3: Congrats!**&#x20;

* Now you're waiting in the Entry Queue [https://www.validatorqueue.com](https://www.validatorqueue.com/)

<!---->

* Check out the [next steps from the main guide](https://www.coincashew.com/coins/overview-eth/guide-or-how-to-setup-a-validator-on-eth2-mainnet/part-i-installation/step-5-installing-validator/next-steps) for further knowledge. Especially the FAQ's "Wen staking rewards?"

</details>

## :joy: POAP

Are you a EthPillar Enjooyer? [Support this public good by purchasing a limited edition POAP!](https://checkout.poap.xyz/169495)

<figure><img src="../../.gitbook/assets/3adf69e9-fb1b-4665-8645-60d71dd01a7b.png" alt=""><figcaption><p>Your EthPillar Enjoyoor's POAP</p></figcaption></figure>

**Purchase link:** [https://checkout.poap.xyz/169495](https://checkout.poap.xyz/169495)

ETH accepted on Mainnet, Arbitrum, Base, Optimism. :pray:

## :telephone: Get in touch

Have questions? Chat with other home stakers on [Discord](https://discord.gg/w8Bx8W2HPW) or open PRs/issues on [Github](https://github.com/coincashew/ethpillar).

## :heart: Donations

If you'd like to support this public goods project, find us on the next Gitcoin Grants.

Our donation address is [0xCF83d0c22dd54475cC0C52721B0ef07d9756E8C0](https://etherscan.io/address/0xCF83d0c22dd54475cC0C52721B0ef07d9756E8C0) or coincashew.eth

## :ballot\_box\_with\_check: How to Update

{% tabs %}
{% tab title="TUI Update" %}
Upon opening EthPillar,

* Navigate to **System Administration > Update EthPillar** and then quit and relaunch.
{% endtab %}

{% tab title="Manual Update" %}
From a terminal, pull the latest updates from git.

```bash
cd ~/git/ethpillar
git pull
```
{% endtab %}
{% endtabs %}
