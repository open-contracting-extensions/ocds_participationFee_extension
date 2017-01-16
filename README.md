# Participation fees

## Background

Whilst Open Contracting principles would encourage governments to make tender documents available free of charge, this is not always the case. Sometimes documents are only available on application or on payment of a fee. Fees can also apply to submit bids or to the winning bidder.

## Extension fields

This extension adds a ```participationFees``` field to the ```tender``` section of OCDS and introduces a new ```participationFee``` building block.

The ```participationFees``` field is an array of ```participationFee``` building blocks.

The ```participationFee``` building block is made up of two fields:

* ```type``` - a value from the ```participationFeeType``` codelist, describing the type of the fee
* ```value``` - the amount and currency of the fee

## Extension codelists

This extension adds **closed** ```participationFeeType``` codelist with the following codes:

* document - a fee payable for access to bidding documents
* submission - a fee payable for the submission of bids
* win - a fee payable by the winning bidder

## Example

The following JSON snippet models a contracting process where fees are applicable for both access to documents and submission of bids:

```JSON
"tender": {
    "participationFees": [
      {
          "type":"document",
          "value": {
               "currency":"GBP",
               "amount":8.00
           } 
      {
          "type":"submission",
          "value": {
               "currency":"GBP",
               "amount":10.00
           } 
    ]
}
```

## To do

* participation / submission terminology
* finalise codelist
