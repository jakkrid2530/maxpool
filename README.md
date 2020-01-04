# maxpool
EthDcrMiner64.exe -epool stratum.okpool.me:3333 -ewal Maxsky -eworker max_pool -epsw x -asm 2 -dbg -1 -allpools 1 -mode 1
{
        "available":37.11827078,
        "balance":37.11827078,
        "currency":"EOS",
        "hold":0
    },
    {
        "available":0,
        "balance":0,
        "currency":"XMR",
        "hold":0
    }

{
    "account_type": "0",
    "balance": 0.00878181,
    "valuation_currency": "BTC",
    "timestamp": "2019-12-09 10:28:23"
}

{
    "data": {
        "sub_account": "Test",
        "asset_valuation": 0.00003463,
        "account_type:futures": [
            {
                "balance": 0.00000245,
                "max_withdraw": 0.00000245,
                "currency": "BTC",
                "underlying": "BTC_USD",
                "equity": 0.00000245
            },
            {
                "balance": 1.053473,
                "max_withdraw": 1.053473,
                "currency": "XRP",
                "underlying": "XRP_USD",
                "equity": 1.053473
            }
        ],
        "account_type:spot": [
            {
                "balance": 0.000312544038152,
                "max_withdraw": 0.000312544038152,
                "available": 0.000312544038152,
                "currency": "USDT",
                "hold": 0
            }
        ]
    }
}

POST /api/account/v3/transfer
POST /api/account/v3/transfer{"currency":"etc","amount":1.5,"from":6,"to":3,"to_instrument_id":"btc-usdt"}(usdt is transferred from the Funding account to the delivery btc-usdt futures account)
POST /api/account/v3/transfer{"currency":"eth","amount":1.5,"from":3,"to":1,"instrument_id":"btc-usdt"}(usdt transfers from the btc-usdt futures account to the spot account)
POST /api/account/v3/transfer{"currency":"btc","amount":1.5,"from":6,"to":3}（Btc transfer from Funding account to delivery btc-usd futures account)

GET /api/account/v3/withdrawal/history

{
        "amount":0.094,
        "withdrawal_id": "4703879",
        "fee":"0.01000000eth",
        "txid":"0x62477bac6509a04512819bb1455e923a60dea5966c7caeaa0b24eb8fb0432b85",
        "currency":"ETH",
        "from":"13426335357",
        "to":"0xA41446125D0B5b6785f6898c9D67874D763A1519",
        "timestamp":"2018-04-22T23:09:45.000Z",
        "status":2
    },
    {
        "amount":0.01,
        "withdrawal_id": "4703879",
        "fee":"0.00000000btc",
        "txid":"",
        "currency":"BTC",
        "from":"13426335357",
        "to":"13426335357",
        "timestamp":"2018-05-17T02:43:08.000Z",
        "status":2
    }

GET /api/account/v3/withdrawal/fee
{
        "currency":"BTC",
        "max_fee":0.02,
        "min_fee":0.0005
    },
    {
        "currency":"LTC",
        "max_fee":0.2,
        "min_fee":0.001
    },
    {
        "currency":"ETH",
        "max_fee":0.2,
        "min_fee":0.01
    }
{
        "currency":"XMR",
        "max_fee":0.02,
        "min_fee":0.0005
    }
