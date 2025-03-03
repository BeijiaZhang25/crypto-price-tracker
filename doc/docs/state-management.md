


# State Management with React Query
**`docs/docs/state-management.md`**


# 

## Why React Query?
React Query simplifies API data management:
- Efficient caching (reduces unnecessary API calls).
- Automatic refetching when needed.
- Built-in error handling.


## Implementation in Code
We use `useQuery` to fetch cryptocurrency prices:

```ts
export const useCryptoPrices = () => {
  return useQuery({
    queryKey: ["cryptoPrices"],
    queryFn: () => fetchCryptoPrices(["bitcoin", "ethereum", "dogecoin", "cardano", "solana"]),
    staleTime: 60000, // Cache results for 1 min
  });
};
