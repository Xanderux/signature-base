[![Build Status](https://travis-ci.org/Neo23x0/signature-base.svg?branch=master)](https://travis-ci.org/Neo23x0/signature-base)

# Signature-Base

Signature-Base is the YARA signature and IOC database for our scanners [LOKI](https://github.com/Neo23x0/Loki) and [THOR Lite](https://www.nextron-systems.com/thor-lite/)

## Focus of Signature-Base

1. High quality YARA rules and IOCs with minimal false positives
2. Clear structure
3. Consistent rule format

## Directory Structure

- iocs - Simple IOC files (CSV)
- yara - YARA rules
- threatintel - Threat Intel API Receiver (MISP, OTX)
- misc - Other input files (not IOCs or signatures)

## External Variables in YARA Rules

Using the YARA rules in a tool other than [LOKI](https://github.com/Neo23x0/Loki) or [THOR Lite](https://www.nextron-systems.com/thor-lite/) will cause errors stating an `undefined identifier`. The rules that make use of external variables have been moved to the following 4 files:

- ./yara/generic_anomalies.yar
- ./yara/general_cloaking.yar
- ./yara/thor_inverse_matches.yar
- ./yara/yara_mixed_ext_vars.yar

Just remove these files in case you see the above error message.

## High Quality YARA Rules Feed

If you liked my rules, please check our [commercial rule set and rule feed service](https://www.nextron-systems.com/2018/12/21/yara-rule-sets-and-rule-feed/), which contains better and 20 times the number of rules.

## FAQs

### How can I report false positives?

Use the issues section of this repository.

### How can I help with bugs in rules?

Navigate to the file in this repository. Click on the "edit" symbol in the upper right corner. Edit the file and create a pull request.

### How can I provide a YARA rule or IOCs?

I accept pull requests. See this [thread](https://twitter.com/cyb3rops/status/1320657673742897153) for some help on how to create such a request. 

### What are the differences between THOR Lite and LOKI?

See our comparison table [here](https://www.nextron-systems.com/compare-our-scanners/).

## License

On 13.08.2021 this repository switched its license to "Detection Rule License (DRL) 1.1" (URL: [https://raw.githubusercontent.com/Neo23x0/signature-base/master/LICENSE](https://raw.githubusercontent.com/Neo23x0/signature-base/master/LICENSE)). The last version of the rule set released under the old CC-BY-NC can be found [here](https://github.com/Neo23x0/signature-base/releases/tag/v2.0).

All signatures and IOC files in this repository, except the YARA rules that explicitly indicate a different license (see "license" meta data), are licensed under the [Detection Rule License (DRL) 1.1](https://raw.githubusercontent.com/Neo23x0/signature-base/master/LICENSE).
