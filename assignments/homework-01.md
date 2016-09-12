## Name: sheema rohi

## ip address: 45.55.66.199

## link to my phpmyadmin page:http://45.55.66.199/phpmyadmin

# gift_options.mysql

```
CREATE TABLE IF NOT EXISTS `gift_options` (
  `itemId` int(64) NOT NULL,
  `allowGiftWrap` tinyint(1) NOT NULL,
  `allowGiftMessage` tinyint(1) NOT NULL,
  `allowGiftReceipt` tinyint(1) NOT NULL,
  PRIMARY KEY (`itemId`)
) ENGINE=InnoDB DEFAULT CHARSET=latin1;
```
# image_entities.sql

```
CREATE TABLE IF NOT EXISTS `image_entities` (
  `itemId` int(64) NOT NULL DEFAULT '0',
  `thumbnailImage` varchar(256) NOT NULL,
  `mediumImage` varchar(256) NOT NULL,
  `largeImage` varchar(256) NOT NULL,
  `entityType` varchar(16) NOT NULL,
  PRIMARY KEY (`itemId`)
) ENGINE=InnoDB DEFAULT CHARSET=latin1;
```

# market_place_price.sql

```
CREATE TABLE IF NOT EXISTS `market_place_price` (
  `itemId` int(64) NOT NULL,
  `price` float(6,3) NOT NULL,
  `sellerInfo` varchar(64) NOT NULL,
  `standardShipRate` float(4,2) NOT NULL,
  `twoThreeDayShippingRate` float(4,2) NOT NULL,
  `availableOnline` tinyint(1) NOT NULL,
  `clearance` tinyint(1) NOT NULL,
  `offerType` varchar(32) NOT NULL,
  PRIMARY KEY (`itemId`)
) ENGINE=InnoDB DEFAULT CHARSET=latin1;
```
# products.sql

```
CREATE TABLE IF NOT EXISTS `products` (
  `itemId` int(64) NOT NULL,
  `parentItemId` int(64) NOT NULL,
  `name` varchar(128) NOT NULL,
  `salePrice` float(5,2) NOT NULL,
  `upc` varchar(64) NOT NULL,
  `categoryPath` varchar(64) NOT NULL,
  `shortDescription` text NOT NULL,
  `longDescription` text NOT NULL,
  `brandName` varchar(64) NOT NULL,
  `thumbnailImage` varchar(128) NOT NULL,
  `mediumImage` varchar(128) NOT NULL,
  `largeImage` varchar(128) NOT NULL,
  `productTrackingUrl` varchar(128) NOT NULL,
  `modelNumber` varchar(64) NOT NULL,
  `productUrl` varchar(128) NOT NULL,
  `categoryNode` varchar(64) NOT NULL,
  `stock` varchar(64) NOT NULL,
  `addToCartUrl` varchar(128) NOT NULL,
  `affiliateAddToCartUrl` varchar(128) NOT NULL,
  `offerType` varchar(64) NOT NULL,
  `msrp` float(6,2) NOT NULL,
  `standardShipRate` float(4,2) NOT NULL,
  `color` varchar(64) NOT NULL,
  `customerRating` float(7,3) NOT NULL,
  `numReviews` int(64) NOT NULL,
  `customerRatingImage` varchar(64) NOT NULL,
  `maxItemsInOrder` int(16) NOT NULL,
  `size` varchar(64) NOT NULL,
  `sellerInfo` varchar(64) NOT NULL,
  `age` varchar(64) NOT NULL,
  `gender` varchar(16) NOT NULL,
  `isbn` int(64) NOT NULL,
  `preOrderShipsOn` varchar(64) NOT NULL,
  PRIMARY KEY (`itemId`)
) ENGINE=InnoDB DEFAULT CHARSET=latin1;
```
