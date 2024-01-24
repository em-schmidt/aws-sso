# sso credential provider

A credential provider for the cognitect aws library that implements AWS SSO, suitable for use as a standalone credential provder or in a provider chain.

Provides a default chain that adds SSO to the chain in the same order as other v2 SDKs.

## Include

### deps

```edn
{:deps 
  {io.github.em-schmidt/aws-sso 
    {:git/sha "<latest version>"
     :git/url "https://github.com/em-schmidt/aws-sso"}

```

## Usage

### standalone

```clj
(require [aws-sso.credentials :as sso])
(aws/client {:api sts :credential_provider (sso/sso-credentials-provider)})
```

### provider chain

```clj
(require [aws-sso.credential :as sso])
(aws/client {:api sts :credential_provider (sso/provider-chain)})
```


## See also
https://github.com/cognitect-labs/aws-api/issues/182
https://gist.github.com/lukaszkorecki/120008f7832e23702e94f4205b8e3df5#file-sso-profile-clj


