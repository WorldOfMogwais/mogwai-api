# mogwai-api v1.0
Lightweight API to support World Of Mogwai mobile phone instances

This repository is a collection of reference API implementations for the World of Mogwai mobile phone game.

You do not need to run all the code in this repository, just the code in the language of your choice.  Each language will provide the same interface and return the same data.

You may write your own. Any API that conforms to the specification in this document, and returns the same results as the reference implementation(s) can be considered a valid mogwai-api.

# routes
A valid mogwai-api implementation MUST provide the following RESTful API routes.  

For simplicity, all routes use GET.

In the following, the input types are as follows:
* :address is a valid Mogwai address ("Base58" string)
* :height is a non-negative integer
* :numblocks is a positive integer
* :hex is a hexidecimal string (without leading 0x)

## getbalance
GET /getbalance/:address

## listtransactions
GET /listtransactions/:address

## listmirrtransactions
GET /listmirrtransactions/:address

## getblock
GET /getblock

GET /getblock/:height

## getblocks
GET /getblock/:height/:numblocks

## getevents
GET /getevents/:height/:numblocks

## sendrawtransaction
GET /sendrawtransaction/:hex