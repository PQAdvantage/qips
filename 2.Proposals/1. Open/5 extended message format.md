<pre>
  QIP: 5
  Layer: qrl-node
  Title: Extending message transaction functionality 
  Author: Peter Waterland
  Comments-Summary: 
  Comments-URI: https://github.com/theQRL/qips/pull/8
  Status: draft
  Type: 
  Created: 21/02/2019
</pre>


## Abstract

Message transactions sent on the QRL blockchain network allow broadcast and decentralised storage of 80 bytes of data per transaction for purposes such as notarisation and data stamping. This minor QIP extends the message transaction format to include an optional payee/receipt address.

## Motivation

It would be useful to direct message transactions to a specific destination address rather than simply writing them into the chain in a broadcast manner.

Potential benefits include: 
1) allowing message-based interaction between user and smart contract addresses 
2) enabling user addresses to exchange message data directly between themselves

For example a smart contract may be scripted to perform certain actions based upon specific message transaction input from a given address. Or a smart contract address associated with a user address could alert a user address with a message transaction if certain thresholds are met (such as changes in balance) or to acknowledge receipt of a payment from a user address to a payee contract address.  

Adding a destination address also allows future consensus voting within the QRL network to be refined. (i.e. voting for a specific QIP proposal, contentious network decision or election of addresses to positions of authority within smart contract constructions such as multisignature contract wallets).

## Implementation

Whilst a minor extension to the existing message transaction format this is not backwards compatible with existing versions of qrl-node and therefore requires a hard fork.
