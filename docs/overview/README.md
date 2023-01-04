# Overview

* e-Signet is envisioned to act as a thin add-on system to any existing digital ID solution to bring in additional capabilities

* It is an [OpenID Connect](https://openid.net/connect/) and [OAuth 2.0](https://oauth.net/2/) compliant system which helps relying party to perform quick and simple integration for user verification

* System supports only the secure options in OpenID connect like `authorization code flow` to ensure the resident data is handled securely

* Integrated with [SBI](https://standards.ieee.org/ieee/3167/10925/) (Secure Biometric Interface) to facilitate secure collection of biometrics for the biometric based user verification

* System supports multiple authentication factors like OTP, Biometrics etc. to be inclusive for all types of people

* All integrations to ID system is taken as a runtime pluggable libraries to allow reuse of official container images which helps with easier upgrades

* Since this is designed specifically for country scale resident verification, we don't support additional features like role management, session management etc. 
