# Test Report

## Scope

The scope of testing is to verify fitment to the specification from the perspective of:

* Functionality  
* Deployability  
* Configurability  
* Customizability

Verification is performed not only from the end-user perspective but also from the System Integrator (SI) point of view. Hence, the configurability and extensibility of the software is also assessed. This ensures readiness of software for use in multiple countries. Since MOSIP is an “API First” product platform, verification scope required comprehensive automation testing for all the MOSIP APIs. An automation Test Rig is created for the same. 

The e-Signet testing scope revolves around the following flows:

* Login with OTP
* Login with Biometrics (mock)
* QR code login flow 
* Multi-language support
* Recaptcha validation
* Multiple instances of e-Signet
* Cross-browser testing: e-Signet flow verification in different browsers (Chrome, Microsoft Edge, Firefox, Safari)

## Test Approach

Persona based approach has been adopted to perform the IV&V(Independent Verification and Validation) by simulating the test scenarios that resemble a real-time implementation. 

A Persona is a fictional character/ user profile created to represent a user type that might use a product/ or a service in a similar way. Persona based testing is a software testing technique that puts software testers in the customer's shoes, assesses their needs from the software and thereby determines use cases/ scenarios that the customers will execute. The persona needs may be addressed through any of the following:

* Functionality  
* Deployability  
* Configurability  
* Customizability

The verification methods may differ based on how the need was addressed. 

For regression check, `MOSIP Test Rig`, an automation testing suite is indigenously designed and developed for supporting persona based testing. MOSIP Test Rig covers the end-to-end test execution and reporting. The end-to-end functional test scenarios are written starting from pre-registration, to creation of packet in registration center, processing the packet through the registration processor, generating UIN and authenticating identity using IDA through various permutation and combinations of cases being covered. MOSIP Test Rig will be an open source artifact which can also be enhanced and used by countries to validate the SI deliveries before going live. Persona classes include both negative and positive personas. Negative persona classes include users like Bribed Registration Office, Malicious Insider etc. The needs of positive persona classes must be met, whereas the needs of negative persona classes must be effectively restricted by the software.

## Verified configuration 

Verification is performed on various configurations as mentioned below:

* Default configuration- with 3 Lang 
* Virtual countries
   * 1 Lang configuration
   * 2 Lang configuration
   * 3 Lang configuration

## Feature health

![](\_images/esignet-feature-health.png)

## Functional test results for e-Signet

Below are the test metrics by performing functional testing for e-Signet using `mockMDS`, `mockAuth` and `mockABIS`. The process followed was black box testing which based its test cases on the specifications of the software component under test. Functional test was performed in combination of individual module testing as well as integration testing. Test data were prepared inline with the user stories. Expected results were monitored by examining the user interface. The coverage includes GUI testing, System testing, End-To-End flows across multiple languages and configurations. The testing cycle included simulation of multiple identity schema and respective UI schema configurations.


| **Total**  | **Passed** |  **Failed** | **Skipped** |
|------------|------------|-------------|-------------|
|            |            |             |             |


## External API verification results for e-Signet

Below section provides details on API test metrics for e-Signet by executing MOSIP functional automation Framework. The external API test executions were performed at module level isolation. Each end point is tested with the test data and expectations of each test data are mapped to assert the test case.

| **Total**  | **Passed** |  **Failed** | **Skipped** |
|------------|------------|-------------|-------------|
|            |            |             |             |








## Test Execution Statistics

#### Functional Testing

* Stories Verified: 10
* Test cases: 401
  * Passed: 386
  * Failed: 9
  * Skipped: 6
* Test Rate: 98% With Pass Rate: 97%

#### Device Based Testing

* Test cases: 12
  * Passed: 11
  * Failed: 1
  * Skipped: 0
* Test Rate: 100% With Pass Rate: 91%

#### API Testing

* Test cases: 261
  * Passed: 261
  * Failed: 0
  * Skipped: 0