# Leaf
[![Leaf CI](https://github.com/mandarineorg/leaf/workflows/Unit%20Tests/badge.svg)](https://github.com/mandarineorg/leaf)

<img src="https://www.mandarinets.org/assets/images/full-logo-simple.svg" width="180" height="180" />

A fake file system for [Deno](https://deno.land) binaries by [Mandarine](https://deno.land/x/mandarinets).

------------

## Description
Leaf is a fake file system for Deno binaries. This means, you can save your files along with the binary generated by `deno compile`, this way, you can put all your files together in a single executable which leads to easier deployments and a more compacted deliverable output.

## Usage
To use **Leaf** in your application, you must use the Leaf File System APIs instead of Deno's.

### readFileSync
Synchronously reads and returns the entire contents of a file as an array of bytes. `TextDecoder` can be used to transform the bytes to string if required. Reading a directory returns an empty data array.

```typescript
import { Leaf } from "https://deno.land/x/leaf@v1.0.0/mod.ts";

const decoder = new TextDecoder("utf-8");
const data = Leaf.readFileSync("hello.txt");
console.log(decoder.decode(data));
```

### readFile
Reads and returns the entire contents of a file as an array of bytes. `TextDecoder` can be used to transform the bytes to string if required. Reading a directory returns an empty data array.

```typescript
import { Leaf } from "https://deno.land/x/leaf@v1.0.0/mod.ts";

const decoder = new TextDecoder("utf-8");
const data = await Leaf.readFile("hello.txt");
console.log(decoder.decode(data));
```

### readTextFileSync
Synchronously reads and returns the entire contents of a file as utf8 encoded string.
```typescript
import { Leaf } from "https://deno.land/x/leaf@v1.0.0/mod.ts";

const data = Leaf.readTextFileSync("hello.txt");
console.log(data);
```

### readTextFile
Reads and returns the entire contents of a file as utf8 encoded string.
```typescript
import { Leaf } from "https://deno.land/x/leaf@v1.0.0/mod.ts";

const data = await Leaf.readTextFile("hello.txt");
console.log(data);
```

## Questions
For questions & community support, please visit our [Discord Channel](https://discord.gg/qs72byB) or join us on our [twitter](https://twitter.com/mandarinets).

## Want to help?
### Interested in coding
In order to submit improvements to the code, open a PR and wait for it to review. We appreciate you doing this.
### Not interested in coding
We would love to have you in our community, [please submit an issue](https://github.com/mandarineorg/leaf/issues) to provide information about a bug, feature, or improvement you would like.

## Follow us wherever we are going
- Author : [Andres Pirela](https://twitter.com/andreestech)
- Website : https://www.mandarinets.org/
- Twitter : [@mandarinets](https://twitter.com/mandarinets)
- Discord : [Click here](https://discord.gg/qs72byB)
