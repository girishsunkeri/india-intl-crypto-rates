# india-intl-crypto-rates
A simple page to get and compare rates between Indian markets and International exchanges.

Try out the [Live demo](https://moonlit-academy-178514.appspot.com/)!

## Starting the server

```
git clone https://github.com/heartz/india-intl-crypto-rates.git
cd india-intl-crypto-rates
npm install
npm start
```

You can then point your browser to  ```localhost:3000```.

## API 

API calls for current price (and sometimes other trade information) for the following Exchanges are available:

* [Bittrex](www.bittrex.com)
* [Bitfinex](www.bitfinex.com)
* [Coinbase](www.coinbase.com)
* [CEX](www.cex.io)
* [Zebpay](www.zebpay.com)
* [Koinex](https://koinex.in) (slightly unstable)

Currently only supports BTC, ETH, BCH and LTC (Except Zebpay which only supports BTC).

To use the API calls:
```
/api/<market>/<ticker>
```
Example:

```
/api/bittrex/btc
```

If no ticker is provided, btc is taken as default.
Some markets such as Zebpay and Koinex display all their data in a single call without any ticker.

You can also check the current INR-USD rates using
```
/api/usd_rate
```

This data is fetched using [Fixer](http://fixer.io/).


## TODO

* Building the Arbitrage calculator.
* Auto update prices every few seconds.
* Add more exchanges


Contact: ranadipheartz@gmail.com | Donations: ETH 0x6e457934449fCd3F8cC7A630013c5FC6A29f26A6
