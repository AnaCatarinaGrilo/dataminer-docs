---
uid: KI_Problem_when_server_name_is_DATAMINER
---

# Problem when DMA server is named DATAMINER

## Affected versions

- Main Release versions from DataMiner 10.4.0 [CU2] onwards.
- Feature Release versions from DataMiner 10.4.5 onwards.

## Cause

From DataMiner 10.4.0 [CU2]/10.4.5 onwards<!-- RN 38182 -->, a change to the user validation causes the built-in user account to no longer have the necessary rights if the computer name is "DATAMINER", resulting in various errors.

## Workaround

Change the computer name. However, note that a new DataMiner license file will need to be generated after you do so. To obtain a license file, contact <dataminer.licensing@skyline.be>.

## Fix

No fix is available yet.

## Description

If the computer name of a DataMiner server is DATAMINER, from DataMiner 10.4.0 [CU2]/10.4.5 onwards, the DMA no longer functions correctly. This issue can have the following symptoms:

- SLProtocol RTEs occur.
- The SLSNMPManager logging mentions `FATAL ERROR: Init Failed, while getting a pointer to SLXml (GetXmlCookie failed) - The client is unknown. (hr = 0x8004028A)`.
- The SLDataMiner logging mentions `Init SNMP Manager V1 failed. Unknown Error (hr = 0x80004005)` and multiple instances of `IDataMiner::NotifyDataMiner|ERR|0|Finished [0x0000000000000242] - NT_SET_PARAMETER by External data with error.  (You don't have permission to perform this action. (hr = 0x800402CC))`.
