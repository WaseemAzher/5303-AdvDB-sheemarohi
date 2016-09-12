# Name: sheema rohi

# ip address: 45.55.66.199

# link to my phpmyadmin page:45.55.66.199/phpmyadmin

# gift_options.mysql

~CREATE TABLE IF NOT EXISTS `gift_options` (
  `itemId` int(64) NOT NULL,
  `allowGiftWrap` tinyint(1) NOT NULL,
  `allowGiftMessage` tinyint(1) NOT NULL,
  `allowGiftReceipt` tinyint(1) NOT NULL,
  PRIMARY KEY (`itemId`)
) ENGINE=InnoDB DEFAULT CHARSET=latin1;~
