<h1 align="center">
  <img alt="sus" src="./assets/sus.png" width="128px"/><br/>
  sus
</h1>

<p align="center">a list of tips and sus things that undermine the ethos of crypto</p>
<br/>

## Circumventing censorship and blocks

- [unblock-dapps](https://github.com/ape-dev-cs/unblock-dapps) - Adblock filter that prevents the frontend from blocking you
- [tweet by @dmihal](https://twitter.com/dmihal/status/1559899152770891776) - Add URLS to browser filters to block checking
- [tweet by @qdqd\_\_\_](https://twitter.com/qdqd___/status/1560261523347734528) - Extension that intercepts and mock requests made by dApps to check if you are sanctioned or not

## Self Hosting your frontend

Since most projects are open source, you can simply download the frontend and run it locally on your own device.

There's an article by Marco Worms on [self-hosting frontends](https://medium.com/iearn/self-hosting-web3-services-299306b706ee) that explains how to do this.

Generally, you probably have to remove the TRM part of the frontend, but I will also fork these repos and remove it myself ig -

### AAVE

[TRM-free fork](https://github.com/Nemusonaneko/aave-interface) by Nemu

### OasisDEX

For Oasis, you can just [clone their repo](https://github.com/OasisDEX/oasis-borrow) and change `USE_TRM_API` to `0` in the `.env` file.

## List of projects that implements address checking, TRM, etc

_pls help me compile dis list i am just a dum llama_

### Tornado Cash

Used to have compliance rules built in, didn't help in the face of USTreasury.

### Ren

Implements TRM in this file: [walletHooks.ts](https://github.com/renproject/bridge-v2/blob/226e6dff097c913df225ba6bf7a0b35d697c7951/src/features/wallet/walletHooks.ts)

### Voltz Protocol

Implements TRM in this file: [services.ts](https://github.com/Voltz-Protocol/voltz-ui/blob/99fe1cf0e13fb418a6a22915723b7d901c6732d6/src/contexts/WalletContext/services.ts)

### OasisDEX

Implements TRM in this file: [get.ts](https://github.com/OasisDEX/oasis-borrow/blob/ef5b3e151a004481641e262a4351021d0dd2f5b9/handlers/risk/get.ts)

> _UPDATE 08-13-2022: [This tweet](https://twitter.com/_apedev/status/1558429699931619329) claims Oasis has removed or lessened the check. The code on GitHub didn't change._

### Balancer

Implements TRM in this file: [sanctions-check.ts](https://github.com/balancer-labs/balancer-api/blob/2c839bcdd5249343c48434410eed505ad1afd13d/lambdas/sanctions-check.ts)

### Pokt Network

Pocket Portal announced that they will lock addresses associated with Tornado Cash [in this announcement](https://www.blog.pokt.network/update-on-tornado-cash/).

### Aave

Implements address screening in this PR: [aave/interface#1017](https://github.com/aave/interface/pull/1017)

Prominent figures like [@sassal0x](https://twitter.com/sassal0x/status/1558326040920936448) and [Justin Sun](https://twitter.com/justinsuntron/status/1558397647165091840) have already been blocked on Aave due to unsolicited Tornado ETH dusting.

> _UPDATE 08-13-2022: The TRM censored versions made it into Aave IPFS frontend, [announced officially by Aave](https://twitter.com/AaveAave/status/1558537736956542978)._

### Flashbots

Updates OFAC blacklist in this PR: [flashbots/rpc-endpoint#90](https://github.com/flashbots/rpc-endpoint/pull/90/)

Flashbots Relay and Builder are OFAC compliant and will remain so in the future according to [this tweet](https://twitter.com/bantg/status/1559948198508118016).

### Uniswap

Uniswap collects data on addresses/hash since this PR: [Uniswap/interface#2623](https://github.com/Uniswap/interface/pull/2623)

Uniswap frontend also collects data using TRM Labs, Amplitude, Google Analytics, pointed out by [this tweet](https://twitter.com/bantg/status/1558456226245132294).

Some whitehat hackers have experienced wrongful blocks on Uniswap, according to [this tweet](https://twitter.com/0xzuberg/status/1558278137620103168).

### dYdX

dYdX has blocked people with open positions from continuing to use the protocol, according to [this tweet](https://twitter.com/exegor/status/1557453734522884097).

### Circle

Blacklisted USDC from addresses related to Tornado Cash right after the OFAC sanction announcement.

