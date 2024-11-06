# User
Properties
- id
- 
User can be 
 1. Farmer
 2. Vendor

# Auction 
- **uctionId** (String): Unique identifier for the auction.
- **productId** (String): Reference to the product being auctioned.
- **farmerId** (String): Reference to the farmer who created the auction.
- **startPrice** (Decimal): The initial price of the product for the auction.
- **currentBidPrice** (Decimal): The current highest bid in the auction.
- **reservePrice** (Decimal): Optional, the minimum price the farmer is willing to accept.
- **startTime** (Timestamp): When the auction starts.
- **endTime** (Timestamp): When the auction will end.
- **status** (Enum): Auction status (e.g., active, ended, canceled).
- **minimumBidIncrement** (Decimal): The minimum amount a new bid must exceed the current highest bid by.
- **highestBidderId** (String): Reference to the user (retailer) who has placed the highest bid.
# Bid
- **bidId** (String): Unique identifier for the bid.
- **auctionId** (String): Reference to the auction for which the bid is placed.
- **retailerId** (String): Reference to the retailer who placed the bid.
- **bidAmount** (Decimal): The amount of the bid.
- **bidTime** (Timestamp): The time when the bid was placed.
- **isWinningBid** (Boolean): Whether this bid is currently the highest.