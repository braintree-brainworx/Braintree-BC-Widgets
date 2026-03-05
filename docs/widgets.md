---
layout: page
title: Widgets Reference
permalink: /docs/widgets/
---

# Widgets Reference

Detailed reference for each payment widget included in Braintree BC Widgets.

---

## Credit Card Widget

Renders Braintree hosted fields for secure credit and debit card collection.

### Options

| Option | Type | Description |
|--------|------|-------------|
| `fields` | `object` | Override default hosted field selectors |
| `styles` | `object` | Hosted field CSS styles |

### Events

| Event | Description |
|-------|-------------|
| `onPaymentMethodReceived` | Fired with a nonce when tokenization succeeds |
| `onError` | Fired when tokenisation fails |
| `onValidityChange` | Fired when field validity changes |

---

## PayPal Widget

Renders a PayPal button using the Braintree PayPal integration.

### Options

| Option | Type | Description |
|--------|------|-------------|
| `flow` | `string` | `'checkout'` (default) or `'vault'` |
| `amount` | `string` | Order total (required for checkout flow) |
| `currency` | `string` | ISO 4217 currency code, e.g. `'AUD'` |
| `buttonStyle` | `object` | PayPal button style overrides |

---

## Google Pay Widget

Renders a Google Pay button for eligible browsers.

### Options

| Option | Type | Description |
|--------|------|-------------|
| `merchantId` | `string` | Google Pay merchant ID |
| `environment` | `string` | `'TEST'` or `'PRODUCTION'` |
| `totalPrice` | `string` | Order total as a string, e.g. `'29.99'` |
| `currencyCode` | `string` | ISO 4217 currency code |

---

## Apple Pay Widget

Renders an Apple Pay button for Safari on Apple devices.

### Options

| Option | Type | Description |
|--------|------|-------------|
| `storeName` | `string` | Display name shown in the Apple Pay sheet |
| `totalAmount` | `string` | Order total as a string |
| `currencyCode` | `string` | ISO 4217 currency code |
| `countryCode` | `string` | ISO 3166-1 alpha-2 country code |

---

## Venmo Widget

Renders a Venmo button for eligible US customers.

### Options

| Option | Type | Description |
|--------|------|-------------|
| `allowDesktop` | `boolean` | Enable Venmo on desktop (default: `false`) |
| `allowNewBrowserTab` | `boolean` | Allow opening Venmo in a new tab |
