---
layout: post
title:  "Acuity Staking Guide"
date:   2020-10-25 02:39:49 +0100
categories: acuity
---

- [Introduction](#introduction)
- [Check prerequisite](#check-prerequisite)
  - [Polkadot.js Browser Extension](#polkadotjs-browser-extension)
  - [Acuity Account](#acuity-account)
- [Create a Acuity Controller Account](#create-a-acuity-controller-account)
- [Stake your ACUs](#stake-your-acus)
- [Payout rewards](#payout-rewards)
- [Stop nominating](#stop-nominating)
  - [Step 1: Stop Nominating](#step-1-stop-nominating)
  - [Step 2: Unbonding an amount](#step-2-unbonding-an-amount)
- [Rebonding before the end of the unbonding period](#rebonding-before-the-end-of-the-unbonding-period)

## Introduction

The Genesis block of the [Acuity network](https://polkadot.acuity.social) was launched on September 3, 2020, as a Proof of Authority (PoA) network.

The 17th October 2020 [Proof of Stake](https://polkadot.acuity.social/#/staking) (PoS) has begun and is ready to receive your nominations for their four validators, which you can find under the following addresses:

    5D7b2wg76R3pwUYWkxwUL7Xq5Sy5aCmpK5vRm6YZ89AvzVkV
    5F9H413D3yDKDzN1cQpXNtYx33s4kJjv8DZnqt84xJKSSHkt
    5EviQu53jsfKGXTvqFaWQEgcjykWodBFCwHN1rKYBrjfULsS
    5EKypbhUk7zhmavdeYnTfXUViTrG47zFKg3yjbArbbxDCGR8

Those four validators are managed by Jonathan Brown ([@bluedroplet](https://twitter.com/bluedroplet/)) the Acuity founder and lead developper.

Those validators are charge free with 0% commission fee.

In this guide you will learn how to:
1. check prerequisite
2. create an Acuity Controller Account
3. stake your ACU tokens
4. payout rewards
5. stop nominating
6. rebonding before the end of the unbonding period


## Check prerequisite

### Polkadot.js Browser Extension
Since it is recommended by Acuity for most users to use the [Polkadot.js Browser Extension](https://polkadot.js.org/extension/) to create their addresses, we are focusing on this method.

Make sure to install the [Polkadot.js Browser Extension](https://polkadot.js.org/extension/) before you get started. You can download the extension for [Chrome/Brave](https://chrome.google.com/webstore/detail/polkadot%7Bjs%7D-extension/mopnmbcafieddcagagdcbnhejhlodfdd) and [FireFox](https://addons.mozilla.org/en-US/firefox/addon/polkadot-js-extension/).

### Acuity Account
You also need an active account on the Acuity network and the corresponding mnemonic seed or backup JSON file to access this account. This account will be call your _"Stash account"_ in this guide.

In order to start staking you need ACU tokens on your _"Stash Account"_. You can buy ACU on [Stex Exchange](https://app.stex.com/en/basic-trade/pair/ETH/ACU) or on the [Acuity Discord](https://discordapp.com/invite/GxD7adN) OTC channel. If you have unclaimed ACU and want to claim them you can follow the [Claiming ACU with MEW/Metamask](https://www.youtube.com/watch?v=IEclNLT2M24) video guide.


## Create a Acuity Controller Account
In order to successfully bond your funds and nominate your validator set, you need a separate account, namely your _“Controller Account”_. You will perform everyday staking operations like changing validators or claiming rewards using this account.

1. To create your _“Controller Account”_, connect to [Acuity Polkadot-JS Apps](https://polkadot.acuity.social/#/) and use the Polkadot.js Browser Extension. Click the plus icon in the top right corner. Then click _“Create new account (root or derived)”_. Now you have two options:
   - derive the new account from your existing account: it will be accessible with the same seed (mnemonic phrase) of the account it was derived from
   - create a new account with a new seed: the new account will be independent from the first one and have a separate seed (mnemonic phrase)

    We prefer the second option, because we want to have independent keys, which is why we have to uncheck the _"Derive new account from existing"_ box at the top. Then, click _“Create account from new seed”_.

2. Write down your mnemonic seed phrase and securely store it. Whoever has access to the mnemonic seed also has access to your funds! Check the box on the bottom and click _“Next step”_.

3. Choose a descriptive name for your Controller account as well as a strong password. Then click _“Add the account with the generated seed”_.

![create-controller-account]({{site.url}}/assets/img/acuity-staking-ctrl-account.gif)

> Congratulations, you successfully created your second Acuity account! You will also find this account under the [Accounts](https://polkadot.acuity.social/#/accounts) menu.

## Stake your ACUs
Before starting the Nomination process, send some funds from your _"Stash Account"_ to your _"Controller Account"_ in order to cover transactions fees (2–3 ACUs should be plenty).

1. The staking menu

    To start the staking process, click _"[Staking](https://polkadot.acuity.social/#/staking)"_ in the top menu bar. On the top you will find different tabs with different information and actions related to your staking operations. Click _“Account actions”_ in order to start the nomination process.

2. Define your accounts

    Now click the _“+ Nominator”_ button.

3. Bond your ACUs

    You need to choose distinct account for _“stash account”_ and _“controller account”_ from the previuosly created accounts.

    Choose the amount of ACUs you want to use for staking under _“value bonded”_.

    Choose a destination account for your rewards under _“payment destination”_. Then click _“next”_ to bond your token.

4. Choose validators

    Simply select the validators of your choice by clicking on them in the left box, make sure to have the auto-selection turned off by switching the button below _“nominated accounts”_. You can unselect them from the right box by clicking on them again. Alternatively, you can also use the search bar in the top to look for specific validators by name or address. Then click _“Bond & Nominate”_.

    Acuity founder validator addresses:

        5D7b2wg76R3pwUYWkxwUL7Xq5Sy5aCmpK5vRm6YZ89AvzVkV
        5F9H413D3yDKDzN1cQpXNtYx33s4kJjv8DZnqt84xJKSSHkt
        5EviQu53jsfKGXTvqFaWQEgcjykWodBFCwHN1rKYBrjfULsS
        5EKypbhUk7zhmavdeYnTfXUViTrG47zFKg3yjbArbbxDCGR8

    Please note that you cannot specify the amount delegated to a particular validator. Your bonded ACUs will be spread out among the validators you selected.

5. Bond & Nominate

    Click _“Sign & Submit”_ in order to conclude your nomination.

![nominating]({{site.url}}/assets/img/acuity-staking-nominating.gif)

>Congratulations, your are now a Nominator on the Acuity network!

## Payout rewards

To claim rewards on [Acuity Polkadot-JS Apps](https://polkadot.acuity.social/), you will need to be in the "Payouts" tab underneath _["Staking"](https://polkadot.acuity.social/#/staking)_, which will list all the pending payouts for your stashes.

To then claim your reward, select the "Payout all" button. This will prompt you to select your stash accounts for payout.

Once you are done with payout, another screen will appear asking for you to sign and submit the transaction, and that is all there is to claiming rewards.

## Stop nominating

The following describes how to stop nominating and retrieve your tokens. Please note that Acuity network have a delayed exit period, called the unbonding period, which serves as a cooldown. You will not be able to transfer your tokens before this period has elapsed.

### Step 1: Stop Nominating

On the [Acuity Polkadot-JS Apps](https://polkadot.acuity.social/) navigate to the _["Staking"](https://polkadot.acuity.social/#/staking)_ tab. On this tab click on the _"Account Actions"_ tab at the top of the screen.

Here, click _"Stop"_ on an account you're staking with and would like to free the funds for.

After you confirm this transaction, your tokens will remain bonded. This means they stay ready to be distributed among nominees again. To actually withdraw them, you need to unbond.

### Step 2: Unbonding an amount

To unbond the amount, click the little gear icon next to the account you want to unbond money for, and select _"Unbond funds"_.

Select the amount you wish to unbond and click _"Unbond"_, then confirm the transaction.

If successful, your balance will show as _"unbonding"_ with an indicator of how many more blocks remain until the amount is fully unlocked.

This unbonding duration period is 7 days on the Acuity network.

Once this process is complete, you will have to issue another, final transaction: Withdraw Unbonded. Then, your transferrable balance will increase by the amount of tokens you've just fully unbonded.

![stop-nominating-unbonding]({{site.url}}/assets/img/acuity-staking-stop-unbond.gif)

## Rebonding before the end of the unbonding period

If you want to rebond your tokens before the unbonding period is over you can do this by issuing a rebond extrinsic. This allows you to bond your tokens that are still locked without waiting until the end of the unbonding period.

In order to do this you will need to issue an extrinsic manually from [Acuity Polkadot-JS Apps](https://polkadot.acuity.social/#/).

Go to the _["Extrinsics"](https://polkadot.acuity.social/#/extrinsics)_ option that's located in the _"Developer"_ dropdown in the top menu.

Before rebonding, you need to change your controller account and set it to your stash account. 

Select the _"staking"_ pallet and the _"setController"_ extrinsic. Select your stash account in both "selected account" and "controller" field. Then click _"Submit Transaction"_.

Select the _"staking"_ pallet and the _"rebond"_ extrinsic. Select your stash account. Enter the amount of tokens that are currently locked in unbonding that you want to rebond. Then click _"Submit Transaction"_.

Confirm the transaction in the next pop-up. Once the transaction is included in the next block your tokens will be rebonded again and you can start staking with them.

Finally you can set your controller account back again from the _["Staking"](https://polkadot.acuity.social/#/staking)_ tab. On this tab click on the _"Account Actions"_ tab at the top of the screen.

Here, click the little gear icon next to the account you want to change the controller, and select _"Change controller account"_. After you confirm this transaction, your controller account is set back to the good one and you can nominate again with your re-bond tokens.

![rebonding]({{site.url}}/assets/img/acuity-staking-rebonding.gif)

---------------

In case you have any questions, need more assistance or simply want to chat, always feel free to reach out to us via #Staking channel on [Acuity Discord](https://discordapp.com/invite/GxD7adN) to discuss!