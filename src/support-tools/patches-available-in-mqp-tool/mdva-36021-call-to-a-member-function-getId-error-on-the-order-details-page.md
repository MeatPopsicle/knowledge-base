---
title: "MDVA-36021: Users get error message when opening order details"
labels: MQP patches,Magento Quality Patches,MQP,QPT,Quality Patches Tool,Support Tools,MQP 1.1.1,Magento Commerce,Magento Commerce Cloud,Adobe Commerce,on-premise,cloud infrastructure,Magento,orders,details,error message,2.4.0,2.4.0-p1,2.4.1,2.4.1-p1,2.4.2,2.4.2-p1
---

The MDVA-36021 patch solves the issue where users get *Call to a member function getId()* error message when trying to open order details. This patch is available when the [Quality Patches Tool (QPT)](https://support.magento.com/hc/en-us/articles/360047139492) 1.1.1 is installed. The patch ID is MDVA-36021. Please note that the issue is scheduled to be fixed in Adobe Commerce version 2.4.4.

## Affected products and versions

**The patch is created for Adobe Commerce version:**

* Adobe Commerce on our cloud infrastructure 2.4.1, 2.4.2

**Compatible with Adobe Commerce versions:**

* Adobe Commerce (all deployment methods) 2.4.0 - 2.4.2-p1

>![info]
>
>Note: the patch might become applicable to other versions with new Quality Patches Tool releases. To check if the patch is compatible with your Adobe Commerce version, run `./vendor/bin/magento-patches status`.

## Issue

When users try to open order details, the following error message is displayed on the order details page in the Admin: *report.CRITICAL: Error: Call to a member function getId() on array in /magento2ce/app/code/Magento/Sales/view/adminhtml/templates/order/totals/tax.phtml:62*.

<ins>Prerequisites</ins>:

The system should have tax settings and orders with specific tax rates.

<ins>Steps to reproduce</ins>:

1. Log in to the Commerce Admin.
1. Go to **Sales** > **Orders** > **Open Order**.

<ins>Expected results</ins>:

The order is opened without any error.

<ins>Actual results</ins>:

You get an error message similar to the following: *report.CRITICAL: Error: Call to a member function getId() on array in /magento2ce/app/code/Magento/Sales/view/adminhtml/templates/order/totals/tax.phtml:62*.

## Apply the patch

To apply individual patches, use the following links depending on your deployment type:

* Adobe Commerce on-premise: [Software Update Guide > Apply Patches](https://devdocs.magento.com/guides/v2.4/comp-mgr/patching/mqp.html) in our developer documentation.
* Adobe Commerce on our cloud infrastructure: [Upgrades and Patches > Apply Patches](https://devdocs.magento.com/cloud/project/project-patch.html) in our developer documentation.

## Related reading

To learn more about quality patches for Adobe Commerce, refer to:

* [Quality Patches Tool released: a new tool to self-serve quality patches](https://support.magento.com/hc/en-us/articles/360047139492).
* [Check if patch is available for your Adobe Commerce issue using Quality patches Tool](https://support.magento.com/hc/en-us/articles/360047125252).

For info about other patches available in QPT, refer to the [Patches available in QPT](https://support.magento.com/hc/en-us/sections/360010506631-Patches-available-in-MQP-tool-) section.
