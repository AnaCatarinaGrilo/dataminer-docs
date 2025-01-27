---
uid: General_Main_Release_10.3.0_CU20
---

# General Main Release 10.3.0 CU20 – Preview

> [!IMPORTANT]
> We are still working on this release. Some release notes may still be modified or moved to a later release. Check back soon for updates!

> [!TIP]
> For information on how to upgrade DataMiner, see [Upgrading a DataMiner Agent](xref:Upgrading_a_DataMiner_Agent).

### Enhancements

#### Failover: Virtual IP address check will now use both a ping and an arp command to check whether an IP address is free [ID 40516]

<!-- MR 10.3.0 [CU20]/10.4.0 [CU8] - FR 10.4.11 -->

Up to now, on systems that do not allow ping commands to be executed, in some cases, the virtual IP address check would incorrectly conclude that the IP address was free and decide to claim it, causing the network interface card to malfunction due to IP addresses not being unique.

From now on, when the virtual IP address check has concluded that the IP address is free after having executed the required number of ping commands, it will double-check by executing an arp command.

### Fixes

#### ReIndexElasticSearchIndexes tool would incorrectly overwrite the existing mapping by the default mappings [ID 40073]

<!-- MR 10.3.0 [CU20]/10.4.0 [CU8] - FR 10.4.11 -->

When the *ReIndexElasticSearchIndexes* tool was run, the existing mappings (which define how types should be handled) would incorrectly be overwritten by the default mappings. From now on, the existing mappings will be correctly passed from source database to destination database.
