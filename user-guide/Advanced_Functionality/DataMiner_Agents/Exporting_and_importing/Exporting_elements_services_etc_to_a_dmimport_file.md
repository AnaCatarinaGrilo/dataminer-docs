---
uid: Exporting_elements_services_etc_to_a_dmimport_file
---

# Exporting elements, services, etc. to a .dmimport file

In the DataMiner Cube Surveyor, you can right-click a view in order to export it, with any elements, services, redundancy groups, documents, SLAs and service templates it contains, to .dmimport format. It is also possible to right-click an element or service directly to export it. The .dmimport package will also contain any related properties, protocols, information templates, trend templates, alarm template and Automation scripts.

1. In the Surveyor right-click menu, select *Actions \> Export*.

   > [!NOTE]
   >
   > - This option is also available from a card’s header menu.
   > - If you do not have the *Config* permission for a particular view, export and import actions will not be available for this view.
   > - If you export from a list of items on a view card, only the item you right-clicked will be included in the export to a .dmimport file.

1. From DataMiner 9.6.3 onwards, in the *Export* window, select *Export to DataMiner package*.

1. In the *Export* window, clear the selection from any items you do not want to include in the export.

   > [!NOTE]
   > If you have selected to include a redundancy group, any elements within that group will automatically be included in the export. Similarly, if you have selected an SLA, the SLA service and its service children will automatically be included.

1. Specify which additional information should be included (if any) using the checkboxes below this:

   - Trend data

   - Alarm data

   - Documents

   - Information events

     > [!NOTE]
     >
     > - Including information events is only possible if alarm data are also exported.
     > - Including information events can make the export take significantly longer.

1. Click *Export*.

1. In the *Save As* window, browse to the location where you want to save the export and click *Save*.

1. In the *Export* window, check the progress messages until the export is ready, and click *Finish*.

> [!NOTE]
> If any invalid items are encountered during the export, these will be skipped and a log entry will be created in the SLNet log file.
