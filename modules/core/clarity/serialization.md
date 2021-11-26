# Serialization

`micro-stacks` ships with a number of functions for constructing, serializing and deserializing clarity values. Here are some examples of each:

```
import {
  bufferCV,
  ClarityValue,
  contractPrincipalCV,
  cvToString,
  deserializeCV,
  falseCV,
  IntCV,
  intCV,
  listCV,
  noneCV,
  responseErrorCV,
  responseOkCV,
  serializeCV,
  someCV,
  standardPrincipalCV,
  StringAsciiCV,
  stringAsciiCV,
  StringUtf8CV,
  stringUtf8CV,
  trueCV,
  TupleCV,
  tupleCV,
  UIntCV,
  uintCV,
} from 'micro-stacks/clarity';

// Booleans
const t = trueCV();
const f = falseCV();

// Strings
const asciistr = stringAsciiCV('hello world');
const utf8str = stringUtf8CV('hello 🌾');

// Optionals
const n = noneCV();
const maybeTrue = someCV(trueCV());

// Buffers
const buffer = Buffer.from('this is a test');
const buf = bufferCV(buffer);

// Integers
const int = intCV(-10);
const uint = uintCV(10);

// Principals
const ADDRESS = 'ST1SJ3DTE5DN7X54YDH5D64R3BCB6A2AG2ZQ8YPD5';
const contractName = 'my-contract';
const standardPrincipal = standardPrincipalCV(ADDRESS);
const contractPrincipal = contractPrincipalCV(ADDRESS, 'test-contract');

// Responses
const responseOk = responseOkCV(trueCV());
const responseErr = responseErrorCV(trueCV());

// Lists
const list = listCV([trueCV(), falseCV(), trueCV()]);

// Tuples
const tuple = tupleCV({
  c: trueCV(),
  b: falseCV(),
  a: trueCV(),
});
```
