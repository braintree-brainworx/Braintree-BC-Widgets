---
layout: page
title: Configuration
permalink: /docs/configuration/
---

# Configuration

Configure Braintree BC Widgets to match your store's requirements.

## Global Options

| Option | Type | Default | Description |
|--------|------|---------|-------------|
| `container` | `string` | — | CSS selector for the widget mount point (required) |
| `tokenizationKey` | `string` | — | Braintree tokenization key (required) |
| `paymentMethods` | `string[]` | `['card']` | Payment methods to enable |
| `locale` | `string` | `'en_AU'` | Locale for payment UI |
| `styles` | `object` | `{}` | Custom styles for hosted fields |
| `debug` | `boolean` | `false` | Enable debug logging |

## Payment Methods

| Value | Description |
|-------|-------------|
| `'card'` | Credit and debit card (hosted fields) |
| `'paypal'` | PayPal One Touch |
| `'googlepay'` | Google Pay |
| `'applepay'` | Apple Pay |
| `'venmo'` | Venmo |

## Example Configuration

```javascript
BraintreeBCWidgets.init({
  container: '#payment-container',
  tokenizationKey: 'sandbox_abc123',
  paymentMethods: ['card', 'paypal', 'googlepay'],
  locale: 'en_AU',
  styles: {
    input: {
      'font-size': '16px',
      color: '#333333'
    },
    ':focus': {
      color: '#0070c0'
    },
    '.invalid': {
      color: '#cc0000'
    }
  },
  debug: false
});
```

## Environment

Switch between sandbox and production by providing the appropriate tokenization key from your Braintree control panel. No other configuration change is required.
