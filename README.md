# StockTwits MCP Server

## Overview

The StockTwits MCP server provides a sophisticated social communications platform intended for individuals interested in the markets and investing. It allows developers to integrate rich social features into financial applications or websites, thereby driving engagement and expanding reach through the StockTwits community. The server supports JSON format for API responses and focuses on delivering curated conversation streams around securities and financial topics.

## Key Features

### Authentication
The StockTwits MCP server utilizes OAuth 2.0 for authentication. When a user authorizes your application, you gain access to their StockTwits account. By default, only public data is accessible, but applications can request broader permissions for more extensive access.

### Rate Limits
The server enforces rate limits on API calls. The default rate limit varies based on the authorization method and whether the method requires authentication.

### Error and Response Codes
Responses from the server include JSON objects with HTTP status codes and additional data, such as error messages. This ensures that developers can effectively handle errors with machine-readable codes and descriptive text.

### Display Guidelines
To maintain consistency in integrating StockTwits functionality, developers should adhere to specific display guidelines provided by StockTwits. These guidelines include the use of appropriate logos and graphics.

### Cashtag Linking and Character Counting
Messages on StockTwits revolve around financial securities using cashtags (e.g., $TICKER). The server provides a library for autolinking and extracting cashtags, ensuring messages adhere to character limits and rules.

### StockTwits Symbology
StockTwits supports discussions for nearly 10,000 symbols representing publicly traded equities, Futures, and Forex instruments, using $TICKER cashtags. A regularly updated symbology file is available, listing supported symbols along with their StockTwits ID, exchange, and equity name.

## Tools and Functions

The StockTwits MCP server includes a variety of tools grouped by their functionality:

### Watchlists
- **watchlists/index**: Returns a list of private watchlists for the authenticating user.
- **watchlists/show**: Provides the list of ticker symbols in a specified watchlist, identified by the list's ID.

### Blocks
- **blocks/create**: Blocks a user, preventing the authenticating user from receiving messages from them.
- **blocks/destroy**: Unblocks a user, allowing message reception from them.

### Messages
- **messages/like**: Likes a message on StockTwits on behalf of the authenticating user.
- **messages/show**: Displays details of a specified message.
- **messages/unlike**: Unlikes a message on behalf of the authenticating user.
- **messages/create**: Allows creation of a StockTwits message, with options to upload accompanying charts.

### Streams
- **streams/mentions**: Retrieves the most recent 30 messages containing mentions of the authenticating user's handle.
- **streams/user**: Fetches the most recent 30 messages for a specified user.
- **streams/direct**: Returns the most recent 30 direct messages sent to the authenticating user.
- **streams/home**: Provides the most recent 30 messages posted to the authenticating user's home stream.
- **streams/symbol**: Retrieves the most recent 30 messages for a specified symbol.
- **streams/investor_relations**: Returns messages posted by verified Investor Relations customers.
- **streams/friends**: Fetches messages from the authenticating user's people stream.
- **streams/watchlist**: Provides messages for the specified watchlist of the authenticating user.

## Support

For further assistance, developers can seek help through the discussion forum or contact the team via email for any questions or issues encountered while using the StockTwits MCP server.