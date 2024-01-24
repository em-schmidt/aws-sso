# sso credential provider

A credential provider for the cognitect aws library that implements AWS SSO, suitable for use as a standalone credential provder or in a provider chain.

## Usage

### standalone

```clj
(require sso)
(aws/client {:api sts :credential_provider sso/provider})
```

### provider chain

```clj
(require sso)
(aws/client {:api sts :credential_provider sso/provider-chain})
```


## See also
https://github.com/cognitect-labs/aws-api/issues/182
https://gist.github.com/lukaszkorecki/120008f7832e23702e94f4205b8e3df5#file-sso-profile-clj


