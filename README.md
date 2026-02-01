# Blueberry
Privacy Bitcoin Wallet Server

The new and better electrum server that improves privacy and data consistency by order of magnitude

# Goals
1. MUST: query transaction history without revealing if address has already appeared on the blockchain or is unused
2. BEST EFFORT: provide some kind of quantifiable anonymity set for indexing addresses on bitcoin blockchain transaction history
3. fully replace electrum server protocol while preseving previous two points
4. improve on electrum server by providing blockhash based snapshot of state of blockchain (to handle reorg edge cases)
5. primarily focused for light mobile wallets or block explorers
6. implement paging from newest transaction (provide consistent snapshot accross pages)

# Implementation
1. efficiency: static file based for web caching due to tradeoff between privacy and filesize
2. inspiration: hash bit prefix for privacy preserving leaked password search on https://haveibeenpwned.com/Passwords
