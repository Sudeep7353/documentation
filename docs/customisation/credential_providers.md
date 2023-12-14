# Credential Provider customization

Inji currently provides support for two credential providers:

1. Download via UIN/VID
2. Download via eSignet

To set up a new provider that can issue VC, it can be accomplished by making a few configuration changes. The configuration details can be found in the `mimoto-issuers-config.json` property file. This file is maintained separately for each deployment environment. In this repository, each environment's configuration is stored in a dedicated branch specific to that environment.

> Refer to [mimoto-issuers-config.json](https://github.com/mosip/mosip-config/blob/collab/mimoto-issuers-config.json) of Collab environment.

These values will be used by Inji via Mimoto. Mimoto exposes APIs which is used by the Inji application to fetch and store the issuers and their configurations in the local storage.

* API used to fetch issuers: `https://api.mosip.io/v1/mimoto/residentmobileapp/issuers`
* API used to fetch issuer's configuration: `https://api.mosip.io/v1/mimoto/residentmobileapp/issuers${issuerId}`

In `mimoto-issuers-config.json`, new providers can be added as per the `well-known` schema.

After adding the provider in configuration, it will be displayed on the UI on `Add new card` screen.

* If new provider supports [OpenID4VCI](https://openid.net/specs/openid-4-verifiable-credential-issuance-1_0.html) protocol, it is recommended to use `issuerMachine.ts` and `EsignetMosipVCItemMachine.ts` for workflow to download VC.
  
* If it doesn't support `OpenID4VCI` protocol, new state machine needs to be added. Please refer to `issuerMachine.ts` and `EsignetMosipVCItemMachine.ts`.