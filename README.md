# Magento 2: Search Overlay for Magento 2

## Overview

This is a basic search overlay for default theme and Hyvä Theme built in Magento 2.

## Prerequisites

- PHP 7.4 or later


## Run regular commands

```
composer require sandipchandela/magento2-search-overlay
bin/magento setup:upgrade
bin/magento setup:di:compile
bin/magento setup:static-content:deploy -s
```

## For Injecting 3rd Party Collection

```
di.xml
```
```xml
<type name="Sandip\SearchOverlay\Model\SearchServicePool">
    <arguments>
        <argument name="services" xsi:type="array">
            <item name="faqs" xsi:type="object">Vendor\FaqOverlay\Service\FaqService</item>
        </argument>
    </arguments>
</type>
```
