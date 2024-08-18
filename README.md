# url_encode_and_decode

I don't want to use https://www.urlencoder.org/ anymore because I can't trust its safety.

gist url:
[url_encode_decode](https://gist.github.com/opoojkk/65e3e6382bc95fedb7a94de2b7fbb00f)

## How to Use
Save the Script: Save the provided shell script (url_encode_decode.sh) to your local machine.

## Usage:

-e: URL encode the input string.
-d: URL decode the input string.
Syntax:


```shell
bash url_encode_decode.sh <option> <string>
```
## Options:

-e: Encode the input string to URL format.
-d: Decode the URL encoded string to original format.
## Examples:

Encode: bash url_encode_decode.sh -e "hello world"
Decode: bash url_encode_decode.sh -d "hello%20world"
## Important Notes
Ensure you have necessary permissions to execute the shell script.
This script utilizes xxd command for encoding and decoding operations. Ensure it is available on your system.
