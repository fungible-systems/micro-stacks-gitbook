# Clarity Values

What are clarity values and why do they exist?

Clarity is a strongly-typed language. Its types define both what kind of data can be stored and how data should be formatted within Clarity variables. This language feature means developers need to declare variables and type values correctly but it also ensures that Clarity contracts are very predictable. `micro-stacks` has a full implementation of Clarity Values (CV) as well as a number of helpers to make it easier for developers to focus on the core application functionality.

Here is a brief overview of Clarity's types and their corresponding Clarity Values:

#### Integers (Signed and unsigned)

`int` (signed integer), e.g., `0`, `-220`, `29529342`. The minimum value is `-2^127` and the maximum value is `2^127 - 1`.

`uint` (unsigned integer), e.g., `u0`, `u2962412`.The minimum value is `0` and the maximum value is `2^128 - 1`

#### Booleans

`true` and `false`

#### Principals

The principal type represents a publicly viewable Stacks address. Principals can either be _standard_ principles, which have a corresponding private key, or _contract_ principals that refer to a specific smart contract.

Principals that start with `SP` refer to mainnet and `ST` for testnet and devnet.

#### Buffers

Buffers are stored as hexadecimal values prefixed by `0x`. The following represents the string `Hello World!`&#x20;

`0x48656c6c6f20576f726c6421`&#x20;

#### Strings (ASCII and UTF-8)

String values store a sequence of characters, encoded as either `ASCII` or `UFT-8`.

#### Lists

Lists in Clarity store fixed length sequences of another type and no type mixing is allowed so all items must be of the same type.

#### Optionals

Optionals in Clarity extend the base types to provide a way to accommodate situations where it is desirable to allow for `no value`. Optionals wrap another type and expose its underlying existence by specifying `some` (it exists) and `none` (it doesn't exist).

#### Tuples

Types are Clarity's named field record variable type.

```
{
    messageId: u3, ;; uint
    message: u"micro-stacks is awesome" ;; UTF-8 string
}
```

#### Responses

Response types include `ok` and `err` and indicate whether an action succeeded or failed.
