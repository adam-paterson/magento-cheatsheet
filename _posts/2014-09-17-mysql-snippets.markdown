---
layout: page
title:  "MySQL Snippets"
date:   2014-09-17 15:37:19
categories: database mysql
---

## Customer Data

This will delete all customer data from your store. Including searches, polls, reports and newsletter subscriptions.

{% highlight sql %}
-- Customers
DELETE FROM `customer_address_entity`;
DELETE FROM `customer_address_entity_datetime`;
DELETE FROM `customer_address_entity_decimal`;
DELETE FROM `customer_address_entity_int`;
DELETE FROM `customer_address_entity_text`;
DELETE FROM `customer_address_entity_varchar`;
DELETE FROM `customer_entity`;
DELETE FROM `customer_entity_datetime`;
DELETE FROM `customer_entity_decimal`;
DELETE FROM `customer_entity_int`;
DELETE FROM `customer_entity_text`;
DELETE FROM `customer_entity_varchar`;
ALTER TABLE `customer_address_entity` AUTO_INCREMENT=1;
ALTER TABLE `customer_address_entity_datetime` AUTO_INCREMENT=1;
ALTER TABLE `customer_address_entity_decimal` AUTO_INCREMENT=1;
ALTER TABLE `customer_address_entity_int` AUTO_INCREMENT=1;
ALTER TABLE `customer_address_entity_text` AUTO_INCREMENT=1;
ALTER TABLE `customer_address_entity_varchar` AUTO_INCREMENT=1;
ALTER TABLE `customer_entity` AUTO_INCREMENT=1;
ALTER TABLE `customer_entity_datetime` AUTO_INCREMENT=1;
ALTER TABLE `customer_entity_decimal` AUTO_INCREMENT=1;
ALTER TABLE `customer_entity_int` AUTO_INCREMENT=1;
ALTER TABLE `customer_entity_text` AUTO_INCREMENT=1;
ALTER TABLE `customer_entity_varchar` AUTO_INCREMENT=1;

-- Search
DELETE FROM `catalogsearch_query`;
DELETE FROM `catalogsearch_fulltext`;
DELETE FROM `catalogsearch_result`;
ALTER TABLE `catalogsearch_query` AUTO_INCREMENT=1;
ALTER TABLE `catalogsearch_fulltext` AUTO_INCREMENT=1;
ALTER TABLE `catalogsearch_result` AUTO_INCREMENT=1;

-- Polls
DELETE FROM `poll`;
DELETE FROM `poll_answer`;
DELETE FROM `poll_store`;
DELETE FROM `poll_vote`;
ALTER TABLE `poll` AUTO_INCREMENT=1;
ALTER TABLE `poll_answer` AUTO_INCREMENT=1;
ALTER TABLE `poll_store` AUTO_INCREMENT=1;
ALTER TABLE `poll_vote` AUTO_INCREMENT=1;

-- Reports
DELETE FROM `report_viewed_product_index`;
ALTER TABLE `report_viewed_product_index` AUTO_INCREMENT=1;

-- Newsletter
DELETE FROM `newsletter_queue`;
DELETE FROM `newsletter_queue_link`;
DELETE FROM `newsletter_subscriber`;
DELETE FROM `newsletter_problem`;
DELETE FROM `newsletter_queue_store_link`;
ALTER TABLE `newsletter_queue` AUTO_INCREMENT=1;
ALTER TABLE `newsletter_subscriber` AUTO_INCREMENT=1;
ALTER TABLE `newsletter_problem` AUTO_INCREMENT=1;
ALTER TABLE `newsletter_queue_store_link` AUTO_INCREMENT=1;
{% endhighlight %}


## Logs

{% highlight sql %}
DELETE FROM `log_customer`;
DELETE FROM `log_visitor`;
DELETE FROM `log_visitor_info`;
DELETE FROM `log_visitor_online`;
DELETE FROM `log_quote`;
DELETE FROM `log_summary`;
DELETE FROM `log_summary_type`;
DELETE FROM `log_url`;
DELETE FROM `log_url_info`;
DELETE FROM `sendfriend_log`;
DELETE FROM `report_event`;
DELETE FROM `dataflow_batch_import`;
DELETE FROM `dataflow_batch_export`;
DELETE FROM `index_process_event`;
DELETE FROM `index_event`;
ALTER TABLE `log_customer` AUTO_INCREMENT=1;
ALTER TABLE `log_visitor` AUTO_INCREMENT=1;
ALTER TABLE `log_visitor_info` AUTO_INCREMENT=1;
ALTER TABLE `log_visitor_online` AUTO_INCREMENT=1;
ALTER TABLE `log_quote` AUTO_INCREMENT=1;
ALTER TABLE `log_summary` AUTO_INCREMENT=1;
ALTER TABLE `log_url_info` AUTO_INCREMENT=1;
ALTER TABLE `sendfriend_log` AUTO_INCREMENT=1;
ALTER TABLE `report_event` AUTO_INCREMENT=1;
ALTER TABLE `dataflow_batch_import` AUTO_INCREMENT=1;
ALTER TABLE `dataflow_batch_export` AUTO_INCREMENT=1;
ALTER TABLE `index_event` AUTO_INCREMENT=1;

--
-- Enterprise Edition
--
DELETE FROM `enterprise_logging_event`;
DELETE FROM `enterprise_logging_event_changes`;
ALTER TABLE `enterprise_logging_event` AUTO_INCREMENT=1;
ALTER TABLE `enterprise_logging_event_changes` AUTO_INCREMENT=1;
{% endhighlight %}

## Products
{% highlight sql %}
DELETE FROM TABLE `catalog_product_bundle_option`;
DELETE FROM TABLE `catalog_product_bundle_option_value`;
DELETE FROM TABLE `catalog_product_bundle_selection`;
DELETE FROM TABLE `catalog_product_entity_datetime`;
DELETE FROM TABLE `catalog_product_entity_decimal`;
DELETE FROM TABLE `catalog_product_entity_gallery`;
DELETE FROM TABLE `catalog_product_entity_int`;
DELETE FROM TABLE `catalog_product_entity_media_gallery`;
DELETE FROM TABLE `catalog_product_entity_media_gallery_value`;
DELETE FROM TABLE `catalog_product_entity_text`;
DELETE FROM TABLE `catalog_product_entity_tier_price`;
DELETE FROM TABLE `catalog_product_entity_varchar`;
DELETE FROM TABLE `catalog_product_link`;
DELETE FROM TABLE `catalog_product_link_attribute`;
DELETE FROM TABLE `catalog_product_link_attribute_decimal`;
DELETE FROM TABLE `catalog_product_link_attribute_int`;
DELETE FROM TABLE `catalog_product_link_attribute_varchar`;
DELETE FROM TABLE `catalog_product_link_type`;
DELETE FROM TABLE `catalog_product_option`;
DELETE FROM TABLE `catalog_product_option_price`;
DELETE FROM TABLE `catalog_product_option_title`;
DELETE FROM TABLE `catalog_product_option_type_price`;
DELETE FROM TABLE `catalog_product_option_type_title`;
DELETE FROM TABLE `catalog_product_option_type_value`;
DELETE FROM TABLE `catalog_product_super_attribute`;
DELETE FROM TABLE `catalog_product_super_attribute_label`;
DELETE FROM TABLE `catalog_product_super_attribute_pricing`;
DELETE FROM TABLE `catalog_product_super_link`;
DELETE FROM TABLE `catalog_product_enabled_index`;
DELETE FROM TABLE `catalog_product_website`;
DELETE FROM TABLE `catalog_product_entity`;
DELETE FROM TABLE `cataloginventory_stock`;
DELETE FROM TABLE `cataloginventory_stock_item`;
DELETE FROM TABLE `cataloginventory_stock_status`;
DELETE FROM TABLE `catalog_category_entity`;
DELETE FROM TABLE `catalog_category_entity_datetime`;
DELETE FROM TABLE `catalog_category_entity_decimal`;
DELETE FROM TABLE `catalog_category_entity_int`;
DELETE FROM TABLE `catalog_category_entity_text`;
DELETE FROM TABLE `catalog_category_entity_varchar`;
DELETE FROM TABLE `catalog_category_product`;
DELETE FROM TABLE `catalog_category_product_index`;
DELETE FROM TABLE `catalog_product_relation`;
DELETE FROM TABLE `catalog_product_flat_1`;
DELETE FROM TABLE `catalog_category_flat_store_1`;
DELETE FROM TABLE `catalog_category_flat_store_2`;
DELETE FROM TABLE `catalog_category_flat_store_3`;
{% endhighlight %}

## Sales
{% highlight sql %}
DELETE FROM `sales_payment_transaction`;
DELETE FROM `sales_flat_creditmemo`;
DELETE FROM `sales_flat_creditmemo_comment`;
DELETE FROM `sales_flat_creditmemo_grid`;
DELETE FROM `sales_flat_creditmemo_item`;
DELETE FROM `sales_flat_order`;
DELETE FROM `sales_flat_order_address`;
DELETE FROM `sales_flat_order_grid`;
DELETE FROM `sales_flat_order_item`;
DELETE FROM `sales_flat_order_status_history`;
DELETE FROM `sales_flat_quote`;
DELETE FROM `sales_flat_quote_address`;
DELETE FROM `sales_flat_quote_address_item`;
DELETE FROM `sales_flat_quote_item`;
DELETE FROM `sales_flat_quote_item_option`;
DELETE FROM `sales_flat_order_payment`;
DELETE FROM `sales_flat_quote_payment`;
DELETE FROM `sales_flat_quote_shipping_rate`;
DELETE FROM `sales_flat_shipment`;
DELETE FROM `sales_flat_shipment_item`;
DELETE FROM `sales_flat_shipment_grid`;
DELETE FROM `sales_flat_shipment_track`;
DELETE FROM `sales_flat_invoice`;
DELETE FROM `sales_flat_invoice_grid`;
DELETE FROM `sales_flat_invoice_item`;
DELETE FROM `sales_flat_invoice_comment`;
DELETE FROM `tag`;
DELETE FROM `tag_relation`;
DELETE FROM `tag_summary`;
DELETE FROM `wishlist`;
DELETE FROM `report_event`;
DELETE FROM `catalogsearch_fulltext`;

-- Reports
DELETE FROM `sales_bestsellers_aggregated_daily`;
DELETE FROM `sales_bestsellers_aggregated_monthly`;
DELETE FROM `sales_bestsellers_aggregated_yearly`;
DELETE FROM `sales_invoiced_aggregated`;
DELETE FROM `sales_invoiced_aggregated_order`;
DELETE FROM `sales_order_aggregated_created`;
DELETE FROM `sales_order_aggregated_updated`;
DELETE FROM `sales_refunded_aggregated`;
DELETE FROM `sales_refunded_aggregated_order`;
DELETE FROM `sales_shipping_aggregated`;
DELETE FROM `sales_shipping_aggregated_order`;
DELETE FROM `coupon_aggregated`;
DELETE FROM `review`;
DELETE FROM `review_detail`;
DELETE FROM `review_entity_summary`;
DELETE FROM `rating_store`;

--
-- Enterprise Edition
--
DELETE FROM `enterprise_reward`;
DELETE FROM `enterprise_reward_history`;
DELETE FROM `enterprise_customer_sales_flat_quote_address`;
DELETE FROM `enterprise_customer_sales_flat_quote`;
DELETE FROM `enterprise_customer_sales_flat_order_address`;
DELETE FROM `enterprise_customer_sales_flat_order`;

ALTER TABLE `sales_payment_transaction` AUTO_INCREMENT=1;
ALTER TABLE `sales_flat_creditmemo` AUTO_INCREMENT=1;
ALTER TABLE `sales_flat_creditmemo_comment` AUTO_INCREMENT=1;
ALTER TABLE `sales_flat_creditmemo_grid` AUTO_INCREMENT=1;
ALTER TABLE `sales_flat_creditmemo_item` AUTO_INCREMENT=1;
ALTER TABLE `sales_flat_order` AUTO_INCREMENT=1;
ALTER TABLE `sales_flat_order_address` AUTO_INCREMENT=1;
ALTER TABLE `sales_flat_order_grid` AUTO_INCREMENT=1;
ALTER TABLE `sales_flat_order_item` AUTO_INCREMENT=1;
ALTER TABLE `sales_flat_order_status_history` AUTO_INCREMENT=1;
ALTER TABLE `sales_flat_quote` AUTO_INCREMENT=1;
ALTER TABLE `sales_flat_quote_address` AUTO_INCREMENT=1;
ALTER TABLE `sales_flat_quote_address_item` AUTO_INCREMENT=1;
ALTER TABLE `sales_flat_quote_item` AUTO_INCREMENT=1;
ALTER TABLE `sales_flat_quote_item_option` AUTO_INCREMENT=1;
ALTER TABLE `sales_flat_order_payment` AUTO_INCREMENT=1;
ALTER TABLE `sales_flat_quote_payment` AUTO_INCREMENT=1;
ALTER TABLE `sales_flat_quote_shipping_rate` AUTO_INCREMENT=1;
ALTER TABLE `sales_flat_shipment` AUTO_INCREMENT=1;
ALTER TABLE `sales_flat_shipment_item` AUTO_INCREMENT=1;
ALTER TABLE `sales_flat_invoice` AUTO_INCREMENT=1;
ALTER TABLE `sales_flat_invoice_grid` AUTO_INCREMENT=1;
ALTER TABLE `sales_flat_invoice_item` AUTO_INCREMENT=1;
ALTER TABLE `sales_flat_invoice_comment` AUTO_INCREMENT=1;
ALTER TABLE `sales_flat_shipment_grid` AUTO_INCREMENT=1;
ALTER TABLE `tag` AUTO_INCREMENT=1;
ALTER TABLE `tag_relation` AUTO_INCREMENT=1;
ALTER TABLE `tag_summary` AUTO_INCREMENT=1;
ALTER TABLE `wishlist` AUTO_INCREMENT=1;
ALTER TABLE `report_event` AUTO_INCREMENT=1;
ALTER TABLE `catalogsearch_fulltext` AUTO_INCREMENT=1;

--
-- Enterprise Edition
--
ALTER TABLE `enterprise_reward` AUTO_INCREMENT=1;
ALTER TABLE `enterprise_reward_history` AUTO_INCREMENT=1;
ALTER TABLE `enterprise_customer_sales_flat_quote_address` AUTO_INCREMENT=1;
ALTER TABLE `enterprise_customer_sales_flat_quote` AUTO_INCREMENT=1;
ALTER TABLE `enterprise_customer_sales_flat_order_address` AUTO_INCREMENT=1;
ALTER TABLE `enterprise_customer_sales_flat_order` AUTO_INCREMENT=1;

DELETE FROM `eav_entity_store`;
ALTER TABLE `eav_entity_store` AUTO_INCREMENT=1;
{% endhighlight %}