
Name:
Azharuddin H Mohammad

IP Address
104.236.3.96

Phpmyadmin Link
http://104.236.3.96/phpmyadmin/

***************************************************************

CREATE TABLE IF NOT EXISTS `gift_options` (
  `itemId` int(32) NOT NULL,
  `allowGiftWrap` tinyint(1) NOT NULL,
  `allowGiftMessage` tinyint(1) NOT NULL,
  `allowGiftReceipt` tinyint(1) NOT NULL,
  PRIMARY KEY (`itemId`)
) ENGINE=InnoDB DEFAULT CHARSET=latin1;
***************************************************************

CREATE TABLE IF NOT EXISTS `image_entities` (
  `itemId` int(32) NOT NULL DEFAULT '0',
  `thumbnailImage` varchar(256) NOT NULL,
  `mediumImage` varchar(256) NOT NULL,
  `largeImage` varchar(256) NOT NULL,
  `entityType` varchar(16) NOT NULL,
  PRIMARY KEY (`itemId`)
) ENGINE=InnoDB DEFAULT CHARSET=latin1;
***************************************************************

CREATE TABLE IF NOT EXISTS `market_place_price` (
  `itemId` int(32) NOT NULL,
  `price` float(7,3) NOT NULL,
  `sellerInfo` varchar(64) NOT NULL,
  `standardShipRate` float(6,3) NOT NULL,
  `twoThreeDayShippingRate` float(7,3) NOT NULL,
  `availableOnline` tinyint(1) NOT NULL,
  `clearance` tinyint(1) NOT NULL,
  `offerType` varchar(32) NOT NULL,
  PRIMARY KEY (`itemId`)
) ENGINE=InnoDB DEFAULT CHARSET=latin1;


***************************************************************

CREATE TABLE IF NOT EXISTS `products` (
  `itemId` int(32) NOT NULL,
  `parentItemId` int(32) NOT NULL,
  `name` varchar(64) NOT NULL,
  `salePrice` float(6,2) NOT NULL,
  `upc` varchar(16) NOT NULL,
  `categoryPath` varchar(128) NOT NULL,
  `shortDescription` text NOT NULL,
  `longDescription` text NOT NULL,
  `brandName` varchar(64) NOT NULL,
  `thumbnailImage` varchar(128) NOT NULL,
  `mediumImage` varchar(256) NOT NULL,
  `largeImage` varchar(256) NOT NULL,
  `productTrackingUrl` varchar(1032) NOT NULL,
  `modelNumber` varchar(64) NOT NULL,
  `productUrl` varchar(1032) NOT NULL,
  `categoryNode` varchar(32) NOT NULL,
  `stock` varchar(32) NOT NULL,
  `addToCartUrl` varchar(256) NOT NULL,
  `affiliateAddToCartUrl` varchar(1032) NOT NULL,
  `offerType` varchar(32) NOT NULL,
  `msrp` float(7,2) NOT NULL,
  `standardShipRate` float(5,2) NOT NULL,
  `color` varchar(32) NOT NULL,
  `customerRating` varchar(8) NOT NULL,
  `numReviews` int(8) NOT NULL,
  `customerRatingImage` varchar(64) NOT NULL,
  `maxItemsInOrder` int(8) NOT NULL,
  `size` varchar(64) NOT NULL,
  `sellerInfo` varchar(64) NOT NULL,
  `age` varchar(16) NOT NULL,
  `gender` varchar(16) NOT NULL,
  `isbn` varchar(16) NOT NULL,
  `preOrderShipsOn` varchar(64) NOT NULL,
  PRIMARY KEY (`itemId`)
) ENGINE=InnoDB DEFAULT CHARSET=latin1;
