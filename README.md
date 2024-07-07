![Blnk logo](https://res.cloudinary.com/dmxizylxw/image/upload/v1719884842/blnk-github-logo_twgk1x.png)

## About asset classes

Asset class is used in Blnk to define the currencies of your ledger balances and your transactions. This could mean fiat currencies like the Euro, Dollar, Pound, etc, cryptocurrencies like Bitcoin, Ethereum, etc, or custom asset classes like loyalty points for closed loop systems. 

In the [Blnk Ledger](https://github.com/blnkledger/blnk), the asset class is represented with the `currency` field in its respective endpoints.

## Understanding Precision

Precision is a parameter in Blnk that converts your amount to the lowest unit possible for your asset class.

You can represent the amounts as you wish in your application, however it is crucial to use precision to accurately store fractional amounts in your ledger, avoiding inaccuracy due to floating-point approximations.

>The precision value applied in a transaction depends on the asset class of the transaction. In this repository, you'll find a list of most fiat currencies, and their recommended precision value.

## How to determine a precision value

To apply the right precision value for an asset class, determine the lowest feasible value for the asset class. For most fiat currencies like the Dollar, the lowest value is 0.01 USD, which is 1 cent.

Next, you find how much you need to convert it to an integer. For fiat currencies like the Dollar, it’s precision value is 100.

This means, with a precision value of 100:

- Fractional amount, USD 0.01 is represented as the integer 1.
- Fractional amount, USD 1000.00 is represented as the integer 100000.
- Fractional amount, USD 542.10 is represented as the integer 54210.
- Fractional amount, USD 129.12 is represented as the integer 12912.

## Important to note

100 is not the only precision value for fiat currencies. Most Dinar currencies except the Serbian Dinar have 1,000 subdivisions; this means their precision value is 1000.

However, in two cases, we have currencies with 5 subdivisions — Malagasy Ariary and Mauritanian Ouguiya. In this case, we used 10 as the precision value for easy calculation and reference.

## More Links
- [Visit the Blnk Website](https://blnkfinance.com)
- [Read our developer documentation](https://docs.blnkledger.com)

## Introducing Blnk — the Open-source fintech ledger for the internet

Blnk Ledger is an open-source fintech database for building fintech products to standard and at scale. We designed Blnk to help developers do three things well:

1. Accurately record transactions in their system.
2. Correctly manage complex flow of funds and transaction data.
3. Reliably manage the size of your transactions as your product scales.

## Contribution

Contributions and feedback are welcome and encouraged. Is there a missing fiat currency or an error? Want to create a list for other kinds of currencies? Create a PR or issue, and let us know about it.

You can also join our [Discord community](https://discord.gg/7WNv94zPpx) to do so, and connect with other developers from around the world.