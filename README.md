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
