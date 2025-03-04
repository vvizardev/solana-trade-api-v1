# Solana Trade API ( version 1.0 )

The Solana Data API is a powerful and efficient service designed to fetch and analyze on-chain data, including token transfers, profit and loss (PnL) tracking, sniper bot detection, and more. This API enables developers to integrate real-time Solana insights into their applications, wallets, and analytics dashboards.

[Click to check document](https://solana-exchange.vercel.app/)

It'd be ❤️appreciate if ⭐stared on here

# APIs ( version 1.0 )

## Author
- [`/api/v1`](https://solana-exchange.vercel.app/api/v1)

```
{ "message": "Hello, Solana Trading Center!" }
```

- [`/api/v1/author`](https://solana-exchange.vercel.app/api/v1/author)

```
{ "message":"https://t.me/wizardev" }
```

`Response`
## General
- [`/api/v1/solana/sol_info`](https://solana-exchange.vercel.app/api/v1/solana/sol_info)

```
{
  "success": true,
  "data": {
    "price_usdt": 142.34,
    "price_change_24h": -3.59097,
    "marketcap": 72196219639,
    "marketcap_rank": 6,
    "avg_fee": 0.00002198,
    "min_fee": 0.000005,
    "max_fee": 0.010005
  },
  "metadata": {}
}
```
- [`/api/v1/solana/airdrop/{mint_addr}`](https://solana-exchange.vercel.app/api/v1/solana/airdrop/3MQVpAwsccXHG7k6RvhwBVRCs3tfmHRW8VUYJUdyPBXd)

```
{
  "airdropSig": "5fXqw4QvBCA22WEa5oWhj64QS6GayLep6pd7VA7MzLaKgWLGcbnPVK7VS34KeWddCibLrv1TfsxD6H542jCc8JRF",
  "balance": 32896452699
}
```

## Token
- [`/api/v1/solana/token/mint_info/{mint_address}`](https://solana-exchange.vercel.app/api/v1/solana/token/mint_info/6p6xgHyF7AeE6TZkSmFsko444wqoP15icUSqi2jfGiPN)

```
{
  "created_tx": "3RVpxfaDscntzr4abnmjkkN1cDPthzpxG3Pgt6PksmvhzNDFXxCPPxnKByjPJK4vsmXueD3zxuhYq5PpwCuyigLR",
  "creator": "5e2qRc1DNEXmyxP8qwPwJhRWjef7usLyi7v5xjqLr5G7"
}
```
- [`api/v1/solana/token/rug_check/{mint_address}`](https://solana-exchange.vercel.app/api/v1/solana/token/rug_check/6p6xgHyF7AeE6TZkSmFsko444wqoP15icUSqi2jfGiPN)

```
{
  "creator": "5e2qRc1DNEXmyxP8qwPwJhRWjef7usLyi7v5xjqLr5G7",
  "risks": [
    {
      "name": "Top 10 holders high ownership",
      "value": "",
      "description": "The top 10 users hold more than 70% token supply",
      "score": 9186,
      "level": "danger"
    },
    ...
  ],
  "score": 18595,
  "freezeAuthority": null,
  "mintAuthority": null,
  "tokenMeta": {
    "name": "OFFICIAL TRUMP",
    "symbol": "TRUMP",
    "uri": "https://arweave.net/cSCP0h2n1crjeSWE9KF-XtLciJalDNFs7Vf-Sm0NNY0",
    "mutable": false,
    "updateAuthority": "5e2qRc1DNEXmyxP8qwPwJhRWjef7usLyi7v5xjqLr5G7"
  },
  "price": 13.0614684460392,
  "rugged": false
}
```
## Pumpfun
- [`/api/v1/solana/pumpfun/mint_info/{mint_address}`](https://solana-exchange.vercel.app/api/v1/solana/pumpfun/mint_info/CniPCE4b3s8gSUPhUiyMjXnytrEqUrMfSsnbBjLCpump)

```
{
  "mint": "CniPCE4b3s8gSUPhUiyMjXnytrEqUrMfSsnbBjLCpump",
  "name": "PWEASE",
  "symbol": "pwease",
  "description": "YOU SHOULDA SAID PWEASE ",
  "image_uri": "https://ipfs.io/ipfs/QmboNoCSu87DLgnqqf3LVWCUF2zZtzpSE5LtAa3tx8hUUG",
  "video_uri": null,
  "metadata_uri": "https://ipfs.io/ipfs/QmRnpREFBjET3wXFRTaQAqJ7YK7jiZssZDwJFQ6uHCkEUN",
  "twitter": "https://x.com/TheMisterFrog/status/1895669466786402519",
  "telegram": null,
  "bonding_curve": "EPSQq5tEBonm7yFWo2bYBeCd1bvCsdV8Mq5zDCVvumYP",
  "associated_bonding_curve": "7NFqGn9WPxMHTBh3GDb9dAFmbHVDmXJ7opgZkhMs31Q2",
  "creator": "5ZJQSU7YHuDQqtUhL1z65UUuEnaJJ73J3YCBAo9uuTVD",
  "created_timestamp": 1740949247900,
  "raydium_pool": "9fmdkQipJK2teeUv53BMDXi52uRLbrEvV38K8GBNkiM7",
  "complete": true,
  "virtual_sol_reserves": 115005359770,
  "virtual_token_reserves": 279900000000000,
  "total_supply": 1000000000000000,
  "website": null,
  "show_name": true,
  "king_of_the_hill_timestamp": 1740950695000,
  "market_cap": 111000,
  "reply_count": 1169,
  "last_reply": 1741127522000,
  "nsfw": false,
  "market_id": "A3kVzzqzpa3Xm3W2cMbjyZRpdRhLcp7qUwDqSC5yRisN",
  "inverted": true,
  "is_currently_live": false,
  "username": null,
  "profile_image": null,
  "usd_market_cap": 16075020
}
```
- [`/api/v1/solana/pumpfun/mint_info/similar_token?mint_addr={mint_addr}&limit={number}`](https://solana-exchange.vercel.app/api/v1/solana/pumpfun/similar_token?mint_addr=CniPCE4b3s8gSUPhUiyMjXnytrEqUrMfSsnbBjLCpump&limit=10)

```
[
  {
    "mint": "8u1dkyottYqG9xsK71ySWTnt4sKSy8CFKme2TsSWpump",
    "name": "PWEASE",
    "symbol": "pwease",
    "description": "YOU SHOULDA SAID PWEASE",
    "image_uri": "https://ipfs.io/ipfs/QmVEAMfYqH9z1MRTGCuRWGyvfb24UVpKQGpk4Qjq4e7Cf6",
    "metadata_uri": "https://ipfs.io/ipfs/QmdECtM9vA13VJQJTmHQS5UPzQPiak4uaj28QjYGi6rgmT",
    "twitter": null,
    "telegram": null,
    "bonding_curve": "4v3iFpat3XADpxUFyUoX5yM8NaQgD62GMe7nFUcRk1xi",
    "associated_bonding_curve": "2b4wmkCkAL7mWqLbiboFzqd3t4UZpArDjDPDM7XuebpC",
    "creator": "81KwZDYhTQhg1Ta2VpDvwQDVEzviqPZk4dron6FBhsS1",
    "created_timestamp": 1741125458535,
    "raydium_pool": null,
    "complete": false,
    "virtual_sol_reserves": 31350000004,
    "virtual_token_reserves": 1026794258376857,
    "total_supply": 1000000000000000,
    "website": null,
    "show_name": true,
    "king_of_the_hill_timestamp": null,
    "market_cap": 30.531919854,
    "reply_count": 4,
    "last_reply": 1741125882000,
    "nsfw": false,
    "market_id": null,
    "usd_market_cap": 4434.7613587935
  },
  ...
]
```
- [`/api/v1/solana/pumpfun/reply/{mint_addr}&limit={number}&offset={number}`](https://solana-exchange.vercel.app/api/v1/solana/pumpfun/reply/CniPCE4b3s8gSUPhUiyMjXnytrEqUrMfSsnbBjLCpump?limit=10&offset=0)

```
{
  "replies": [
    {
      "signature": null,
      "is_buy": null,
      "sol_amount": null,
      "id": 106457508,
      "mint": "CniPCE4b3s8gSUPhUiyMjXnytrEqUrMfSsnbBjLCpump",
      "file_uri": null,
      "text": "Can we send this 😂😂😂",
      "user": "831Tnuk8GDfHvjQPdTAG4mou5pc3v5usBCJ6LqNos9fH",
      "timestamp": 1740949319885,
      "total_likes": 8,
      "username": null,
      "profile_image": null,
      "liked_by_user": false
    },
  ...
  ],
  "hasMore": true,
  "offset": 10
```

## Jito
- [`/api/v1/solana/jito/bundle_id?tx_hash={tx_hash}`](https://solana-exchange.vercel.app/api/v1/solana/jito/bundle_id?tx_hash=5ho7ZLqTyNSUWTXqAEDs9uPDAUZ9WuvXSFH1oTU6HTbfDsLffJd6zPDXxE1KHPK7pKmAHqQVEPiGiFDxzpZ2a1Rf)

```
"030ef90c861c6bff073c7aeb74fe4ee127f38819a83862f8a53bd8c747b6c5c7"
```
- [`/api/v1/solana/jito/bundle_info?bundle_id={bundle_id}`](https://solana-exchange.vercel.app/api/v1/solana/jito/bundle_info?bundle_id=030ef90c861c6bff073c7aeb74fe4ee127f38819a83862f8a53bd8c747b6c5c7)
```
{
  "bundleId": "030ef90c861c6bff073c7aeb74fe4ee127f38819a83862f8a53bd8c747b6c5c7",
  "slot": 312220666,
  "validator": "5pPRHniefFjkiaArbGX3Y8NUysJmQ9tMZg3FrFGwHzSm",
  "tippers": [
    "4tUfiHneZjgY5kbwjwdwHWTEnfAUnsXk2TxXT6feyFyr"
  ],
  "landedTipLamports": 1000000,
  "landedCu": 1332001,
  "blockIndex": 1363,
  "timestamp": "2025-01-06T10:01:09Z",
  "txSignatures": [
    "5ho7ZLqTyNSUWTXqAEDs9uPDAUZ9WuvXSFH1oTU6HTbfDsLffJd6zPDXxE1KHPK7pKmAHqQVEPiGiFDxzpZ2a1Rf",
    "5jUoTSoyrYVcFb2BBq2rDcXJUFKh6MtBb81mZW6DN5JZBdPZyRHv25YGF6Y1xgpEykdeXk8UBxFptxV6fgnzaswe",
    "tmUZKih3qUn2LJ7astK7Wt2Dofm1ATpvcSpEA9xjQTMqZuTQz6d9BxCeHY1pCNQewCqhes3MiC2aMBXCuBidaiq",
    "5NR54c4jQyXYEKdCir9Mvafa7LiscM4kCunrRwg4EN25qic2SEfKTVZd5ZJPJ9kpv8CP1zxFx4vzuTtvNUKKzv5g",
    "3X6kywdzmQyA5ZYc1qaUc4LnUg41Sciu3ooGG1jN1qKi1kW5PMmqL2sWZbD9ioZFTkFchstuHxmmdqNeuRFVPuHf"
  ]
}
```
