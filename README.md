Update API_HOST and WS_HOST variable for each environment
## Examples

  * API version
    - Spot: v3.2
    - Futures: v2.1
    - Otc: v1


* [Python]
  * How to play with python examples without docker
    1. Run `cp config/.env.example python/.env` and fill-in needed data in `.env`
    1. Set `python` as your current working directory
    1. install Python (version > 3)
    1. install package by poetry
    1. `python run {{EXAMPLE_FILE}}` to run the example, for example: `python api/spot_get_wallet_balance.py`


* [Nodejs]
  * How to play with node examples without docker
    1. Run `cp config/.env.example nodejs/.env` and fill-in needed data in `.env`
    1. Set `nodejs` as your current working directory
    1. install Nodejs (version > 16)
    1. `npm install` to install required packages
    1. `node {{EXAMPLE_FILE}}` to run the example, for example: `node app/spot/query-market-summary.js`



# Sample File Reference
## Earn
### Investment Endpoints
|Document Name |Python |
| :--------   | :--------   |
|Deposit Investment |earn_buy_product.py |
|Query Investment History |earn_get_history.py |
|Query Investment Orders |earn_get_orders.py |
|Query Investment Products |earn_get_products.py |
|Redeem Investment |earn_redeem_product.py |
|Renew Investment |earn_renew_product.py |
<br>

## Futures
### Public Endpoints
|Document Name |Python | 
| :--------   | :--------   | 
|Market Summary |futures_get_market_summary.py | 
|Charting Data |futures_charting_data.py | 
|Query Market price | futures_query_market_price.py | 
|Orderbook (By grouping) |futures_get_orderbook.py | 
|Orderbook |futures_get_orderbook_L2.py | 
|Query Trades Fills |futures_get_trades.py | 

### Trade Endpoints
|Document Name |Python | 
| :--------   | :--------   | 
|Create new order |futures_place_limit_order.py | 
|Create new algo order|futures_create_new_algo_order.py|
|Amend Order |futures_amend_order.py |
|Cancel Order |futures_cancel_order.py | 
|Dead man's switch (Cancel all after)|futures_cancel_all_after.py|
|Query Open Orders |futures_get_open_orders.py |
|Query Trades Fills|futures_query_trades_fills.py|
|Query Position|futures_query_position.py|query-positions.js|
|Close Position|futures_close_position.py|
|Set Risk Limits|futures_set_risk_limits.py|
|Set Leverage|futures_set_leverage.py|
|Change contract settlement currency|futures_change_settlement_currency.py | 
|Query Account Fees|futures_query_account_fees.py|

### Wallet Endpoints
|Document Name |Python | 
| :--------   | :--------   | 
|Query Wallet Balance|futures_query_wallet_balance.py|
|Query Wallet History | futures_query_wallet_history.py | 
|Query Wallet Margin|futures_query_wallet_margin.py|
|Transfer funds between Futures wallet|futures_transfer_funds_between_futures_wallet.py|

### Websocket Streams
|Document Name |Python |
| :--------   | :--------   |
|Subscription|futures_ws_subscription.py |
|Orderbook Snapshot (By grouping)|futures_ws_get_orderbook_group.py |
|Orderbook Snapshot (By depth)|futures_ws_get_orderbook_depth.py|
|Orderbook Incremental Updates|futures_ws_get_oss_delta.py|
|Public Trade Fills|futures_ws_public_trade_fills.py|
|Authentication|futures_ws_authentication.py|
|Notifications|futures_ws_notifcations.py|
|User Trade Fills|futures_ws_user_trade_fillls.py|
|All Position|futures_ws_get_all_position.py|

## OTC
### OTC Endpoints
|Document Name |Python |
| :--------   | :--------   |
|Market Summary|otc_get_market_summary.py|
|Request for Quote|otc_get_quote.py|
|Accept Quote|otc_accept_quote.py|
|Query Order||

### Websocket Streams
|Document Name |Python |
| :--------   | :--------   |
|Authentication|otc_ws_authentication.py|
|Quote Stream|otc_ws_quote_stream.py|

## Streaming
### Workflow
|Document Name |Python |
| :--------   | :--------   |
|Streaming OTC|streaming_otc.py|

### Websocket Streams
|Document Name |Python |
| :--------   | :--------   |
|Authentication|otc_ws_authentication.py|
|Quote Stream|otc_ws_quote_stream.py|

## wallet/Convert/Transfer
### Public Endpoints
|Document Name |Python |
| :--------   | :--------   |
|Query available crypto network list for currency|queryAvailableCrypo.py|
|Query exchange rate between assets|queryExchangeRate.py|

### Wallet Endpoints
|Document Name |Python |
| :--------   | :--------   |
|Query Wallet Balance|queryWalletBalance.py|
|Query Wallet History|WalletqueryWalletHistory.py|
|Query available currency list for wallet action|queryAvailableCurrency.py|
|Convert funds|WalletConvertFunds.py|
|Transfer funds|WalletTransferFunds.py|
