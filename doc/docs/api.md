


###  **`docs/docs/api.md`** → API Integration  



# API Integration

## CoinGecko API
This app fetches **live cryptocurrency prices** from [CoinGecko API](https://www.coingecko.com/en/api/documentation).

### API Endpoint:
GET https://api.coingecko.com/api/v3/simple/price?ids=bitcoin,ethereum&vs_currencies=usd

### Example Response:
```json
{
  "bitcoin": {
    "usd": 92626
  },
  "ethereum": {
    "usd": 2441.74
  }
}

