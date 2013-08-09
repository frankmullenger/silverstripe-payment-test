# SilverStripe Payment Test Module

## Maintainer Contacts
*  Frank Mullenger 
*  Ryan Dao

## Requirements
* SilverStripe >3.0
* SilverStripe Payment 1.0

## Installation Instructions
1. Place this directory in the root of your SilverStripe installation and call it 'payment-test'.
2. Visit yoursite.com/dev/build to rebuild the database.

## Usage Overview
Enable supported payment methods in your application yaml file, e.g: mysite/_config/payment.yml

```yaml
---
Name: payment
After: 'framework/*','cms/*'
---
PaymentGateway:
  environment:
    'dev'

PaymentProcessor:
  supported_methods:
    dev:
      - 'DummyMerchantHosted'
    live:
      - 'DummyMerchantHosted'
      - 'DummyGatewayHosted'
```
