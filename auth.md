To authenticate an account with our SDK, first you need an `AccountNonce` - use `findAccountByAddressAndChain` to retrieve the nonce.
Then craft a message to sign:

```
Beb.xyz wants you to sign in with your Ethereum account, secured with a signed message:\n ${currentAccount?.nonces?.nonce?.length} ${currentAccount?.nonces?.nonce}
```

Sign this message using metamask, and use `authBySignature` to get an `accessToken`, which you need for authenticated mutations and queries: `Authorization: Bearer $accessToken`.
If you need help, feel free to reach us at [beb.xyz](https://beb.xyz) and by email at gm@beb.xyz!
