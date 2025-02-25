---
title: "MDVA-38308: Error after adding Vimeo videos to disabled products"
labels: MQP patches,Magento Quality Patches,MQP,Support Tools,MQP fixes,Magento Commerce,Magento Commerce Cloud,disabled products,Vimeo,videos,error message,MQP 1.0.26,2.3.5,2.3.4-p2,2.3.5-p1,2.3.5-p2,2.3.6,2.3.6-p1,2.4.0-p1,2.4.1,2.4.1-p1,2.4.2,2.4.2-p1
---

The MDVA-38308 Magento patch solves the issue where users get the error message: *Notice: Undefined index: extension in /lib/internal/Magento/Framework/File/Uploader.php on line 806,* when adding Vimeo videos to disabled products. This patch is available when the [Magento Quality Patch (MQP) tool](https://support.magento.com/hc/en-us/articles/360047139492) 1.0.26 is installed. The patch ID is MDVA-38308. Please note that the issue is scheduled to be fixed in Magento  2.4.4.

## Affected products and versions

**The patch is created for Magento version:**
Magento Commerce Cloud 2.4.1-p1, 2.4.2-p1

**Compatible with Magento versions:**
Magento Commerce and Magento Commerce Cloud 2.3.5 - 2.3.6-p1, 2.4.0 - 2.4.1-p1, 2.4.2 - 2.4.2-p1

>![info]
>
>Note: the patch might become applicable to other versions with new MQP tool releases. To check if the patch is compatible with your Magento version, run `./vendor/bin/magento-patches status`.

## Issue

When adding Vimeo videos to disabled products, you receive the following error message:  *Notice: Undefined index: extension in /lib/internal/Magento/Framework/File/Uploader.php on line 806*

<ins>Steps to reproduce</ins>:

1. Create a simple product.
1. Disable the created product.
1. Try to add a Vimeo video to the disabled product.

<ins>Expected results</ins>:

Video is added without any error.

<ins>Actual results</ins>:

You get the following error:  
*Notice: Undefined index: extension in /lib/internal/Magento/Framework/File/Uploader.php on line 806*

## Apply the patch

To apply individual patches use the following links depending on your Magento product:

* Magento Commerce: DevDocs [Software Update Guide > Apply Patches](https://devdocs.magento.com/guides/v2.4/comp-mgr/patching/mqp.html).
* Magento Commerce Cloud: DevDocs [Upgrades and Patches > Apply Patches](https://devdocs.magento.com/cloud/project/project-patch.html).

## Related reading

To learn more about Magento Quality Patches, refer to:

* [Magento Quality Patches released: a new tool to self-serve quality patches](https://support.magento.com/hc/en-us/articles/360047139492).
* [Check if patch is available for your Magento issue using Magento Quality Patches](https://support.magento.com/hc/en-us/articles/360047125252).

For info about other patches available in MQP tool, refer to the [Patches available in MQP tool](https://support.magento.com/hc/en-us/sections/360010506631-Patches-available-in-MQP-tool-) section.
