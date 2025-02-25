---
title: "MDVA-34591: Cart price rule calculations not as expected"
labels: 2.3.0,2.3.1,2.3.2,2.3.2-p2,2.3.3,2.3.3-p1,2.3.4,2.3.4-p1,2.3.4-p2,2.3.5,2.3.5-p1,2.3.5-p2,2.3.6,2.3.6-p1,2.4.0,2.4.0-p1,2.4.1,2.4.1-p1,2.4.1-p2,2.4.2,MQP 1.0.19,Magento Commerce,Magento Commerce Cloud,Magento Quality Patches,calculation,cart price rule,discount
---

The MDVA-34591 Magento patch fixes the issue where cart price rule with **Maximum Qty Discount is Applied To** does not work correctly if multiple cart price rules are applied.

This patch is available when the [Magento Quality Patch (MQP) tool](https://support.magento.com/hc/en-us/articles/360047139492) 1.0.19 is installed. The patch ID is MDVA-34591. Please note that the issue is scheduled to be fixed in Magento version 2.4.3.

## Affected products and versions

 **The patch is created for Magento version:** Magento Commerce Cloud 2.3.6

 **Compatible with Magento versions:** Magento Commerce and Magneto Commerce Cloud 2.3.0-2.4.2

>![info]
>
>Note: the patch might become applicable to other versions with new MQP tool releases. To check if the patch is compatible with your Magento version, run `./vendor/bin/magento-patches status` .

## Issue

 <span class="wysiwyg-underline">Steps to reproduce</span> :

1. Go to the Admin, and create the following two rules:

* Rule 1:  $10 off a maximum of 3 items in the cart. Set priority = *3* .
* Rule 2:  50% off all products in the cart. Set priority = *1* .

1. Go to the storefront.

1. Add 8 quantities of a product set to price = *$51* each to the cart.

1. Check the discount amount in the cart.

 <span class="wysiwyg-underline">Expected results</span> :

The correct calculated discount is $234, as expected.

* Calculations:

  Matching cart price rules: Rule 2, Rule 1\
  Apply Rule 2 (50% off), so Discount = $204\
  Apply Rule 1 (10 off 3 items), so Discount = $30\
  Total Discount = MIN ( 408/2 + 10x3, 8 &#42; 51) = MIN (204 + 30, 8 &#42; 51) = $234

 <span class="wysiwyg-underline">Actual results</span> :

The discount is incorrectly calculated to be $153, caused by the wrong quantity used for calculating maximum discount value, as the fixed discount amount is applied regardless of the products' amount in the shopping cart.

* Calculations:

  Matching cart price rules: Rule 2, Rule 1\
  Apply Rule 2 (50% off), so Discount = $204\
  Apply Rule 1 (10 off 3 items), so Discount = $30\
  Total Discount = MIN (204 + 30, 3 &#42; 51) = $153

## Apply the patch

To apply individual patches use the following links depending on your Magento product:

* Magento Commerce: DevDocs [Software Update Guide > Apply Patches](https://devdocs.magento.com/guides/v2.4/comp-mgr/patching.html) .
* Magento Commerce Cloud: DevDocs [Upgrades and Patches > Apply Patches](https://devdocs.magento.com/cloud/project/project-patch.html) .

## Related reading

To learn more about Magento Quality Patches, refer to:

* [Magento Quality Patches released: a new tool to self-serve quality patches](https://support.magento.com/hc/en-us/articles/360047139492) .
* [Check patch for Magento issue with Magento Quality Patches](https://support.magento.com/hc/en-us/articles/360047125252) .

For info about other patches available in MQP tool, refer to the [Patches available in MQP tool](https://support.magento.com/hc/en-us/sections/360010506631-Patches-available-in-MQP-tool-) section.
