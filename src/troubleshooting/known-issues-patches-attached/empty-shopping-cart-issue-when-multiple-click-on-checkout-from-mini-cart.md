---
title: Empty shopping cart issue when multiple click on checkout from mini cart
labels: 2.2.3,2.2.5,Magento Commerce,checkout,empty cart,known issues,minicart,patch,troubleshooting
---

This article provides a patch for a known Magento Commerce 2.2.3 issue related to a shopping cart being empty after customers click **Go to Checkout** multiple times in the mini shopping cart.

## Issue

Customers add products to the cart, try to checkout by clicking the **Go to**   **Checkout** button several times, but when they go to the cart, the cart is empty. The mini-cart might still show products.

 <span class="wysiwyg-underline">Steps to reproduce</span> :

1. Open a product page on the store front.
1. Add products to cart.
1. In the mini shopping cart, click **Go to Checkout** several times.

 <span class="wysiwyg-underline">Expected result</span> :

The cart contains all products you have added.

 <span class="wysiwyg-underline">Actual result</span> :

You have no items in your shopping cart.

## Patch

The patches are attached to this article. To download a patch, scroll down to the end of the article and click the required file name, or click one the following links:

 [Download MDVA-10441\_EE\_2.2.3\_v3.composer.patch](assets/MDVA-10441_EE_2.2.3_v3.composer.patch.zip) 

 [Download MDVA-17078\_EE\_2.2.5\_COMPOSER\_v1.patch](assets/MDVA-17078_EE_2.2.5_COMPOSER_v1.patch.zip) 

### Compatible Magento versions

The patches were created for:

* Magento Commerce 2.2.3 (the `MDVA-10441_EE_2.2.3_v3.composer.patch` file)
* Magento Commerce (Cloud) 2.2.5 ( `MDVA-17078_EE_2.2.5_COMPOSER_v1.patch` file)

The `MDVA-10441_EE_2.2.3_v3.composer.patch` patch is also compatible (but might not solve the issue) with the following Magento versions and editions:

* Magento Commerce (Cloud) versions from 2.2.1 to to 2.2.5
* Magento Commerce versions from 2.2.1 to to 2.2.5

The `MDVA-17078_EE_2.2.5_COMPOSER_v1.patch` patch is also compatible (but might not solve the issue) with the following Magento versions and editions:

* Magento Commerce 2.2.5

## How to apply a patch

See [How to apply a composer patch provided by Magento](https://support.magento.com/hc/en-us/articles/360028367731) for instructions.

## Attached Files

 