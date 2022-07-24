To authenticate an account with our SDK, first you need an `AccountNonce` - use `findAccountByAddressAndChain` to retrieve the nonce, which you need for the message.
Then craft this exact message to sign for an Ethereum wallet:

```
Beb.xyz wants you to sign in with your Ethereum account, secured with a signed message:\n ${currentAccount?.nonces?.nonce?.length} ${currentAccount?.nonces?.nonce}
```

Sign this message using the [RainbowKit](https://www.rainbowkit.com/) or [Metamask SDK](https://docs.metamask.io/guide/), and use `authBySignature` to get an `accessToken`, which you need for authenticated mutations and queries: `Authorization: Bearer $accessToken`.

If you get stuck, feel free to reach us at [beb.xyz](https://beb.xyz) and by email at gm@beb.xyz!
