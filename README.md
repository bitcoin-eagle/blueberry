# Blueberry
Privacy Bitcoin Wallet Server

The new and better electrum server that improves privacy and data consistency by order of magnitude

# Goals
1. MUST: query address' transaction history without revealing if address has already appeared on the blockchain or is unused
1. BEST EFFORT: provide some kind of quantifiable anonymity set for indexing addresses on bitcoin blockchain transaction history
1. fully replace electrum server protocol while preseving previous two points
1. improve on electrum server by providing blockhash based consistent snapshot of state of blockchain (to handle reorg edge cases)
1. primarily focused for light mobile wallets or block explorers
1. implement paging from newest transaction first (provide consistent snapshot accross pages)

# Implementation
1. efficiency: static file based for web caching due to tradeoff between privacy and filesize
1. inspiration: hash bit prefix for privacy preserving leaked password search on https://haveibeenpwned.com/Passwords
1. the goals kind of imply that mempool needs to be handled separately and its snapshot updated when chain tip changes or periodically with best effort
