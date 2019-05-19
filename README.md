# Vue Mortgage Calculator

# Overview

Greetings! This goal of this assignment is to test your skills in front-end development.
Your task is to build a mortgage calculator that calculates the total amount that someone
might pay over the course of a 15 or 30 year fixed-rate mortgage.

# Requirements

## Three Inputs - Amount, Interest Rate, Term

- Amount - the whole-number dollar amount for the loan (e.g. \$250,000, no decimals)
- Interest Rate - the interest rate for the loan expressed as a percentage (e.g. 4.5% would be 4.5)
- Term - a dropdown list allowing someone to select a 15 or 30 year fixed mortgage

## Use mortgage.service.js to calculate totals

After you build the inputs, you can use the `mortgage.service.js` to calculate the total amounts.
`mortgage.service.js` has a function named `calculate` that takes `amount, interest, and term`
as arguments, and returns the following object:

```
{
  balance: <some number>,
  pmt: <another number>
}
```

where `balance` is the total amount that someone will pay over the life of their loan, and `pmt`
is the monthly payment that they will have over the life of their loan.

## Display Total Balance, Monthly Payment

Once you have the two total numbers, you should display those beneath your calculator inputs.

# Project setup

The project is already set up for you - this is a standard Vue CLI app without any external
dependencies. You may need to run the project with

```
npm run serve
```

Then navigate to http://localhost:8080/ in your browser.

# Happy coding!

And please feel free to come grab one of us if you have any questions. Our goal is to help you succeed!
