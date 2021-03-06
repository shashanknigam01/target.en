---
keywords: faq;frequently asked questions;analytics for target;a4T;classifications;classification;classifications importer;post-tnt-action
description: This topic contains answers to questions that are frequently asked about classifications and using Analytics as the reporting source for Target (A4T).
title: Classifications - A4T FAQ
feature: a4t troubleshooting
---

# Classifications - A4T FAQ{#classifications-a-t-faq}

This topic contains answers to questions that are frequently asked about classifications and using [!DNL Analytics] as the reporting source for [!DNL Target] (A4T).

## After using the Classifications Importer to download classifications, how do I match the post-tnt-action value with an activity name? {#section_6045DAC488B248418F430E663C38D001}

You can download the classifications for the A4T/TNT string from the Admin Tools [Classification Importer](https://experienceleague.adobe.com/docs/analytics/components/classifications/classifications-importer/c-working-with-saint.html). The variable is called “TNT” in the export list. The downloaded data includes the friendly names for activities, experiences, and so forth.

This lookup file is useful for customers that receive Adobe’s clickstream data feed. The file provides friendly names for the `post_tnt` and `post_tnt_action` columns.

The string format of the TNT variable is `activityID:experienceID:targettype|event`.

* targettype = 0 (control/random) or 1 (targeted) for [!UICONTROL Auto-Allocate] and [!UICONTROL Auto-Target] activities.
* Event = 0 represents an experience entrance. 
* Event = 1 represents an experience visit. 
* Event = 2 represents an activity impression. 
* Event = 3-32766 represents analytics success metric id.
* Event = 32767 represents an activity conversion.

You can import the classification file on a frequent basis from the UI using a [browser import](https://docs.adobe.com/help/en/analytics/components/classifications/classifications-importer/browser-import.html) or an [FTP import](https://docs.adobe.com/help/en/analytics/components/classifications/classifications-importer/import-file.html). You can also engage with Engineering Services to obtain the file as a lookup table along with a clickstream data feed. 
