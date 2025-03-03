
# Challenges & Solutions
**`docs/docs/challenges.md`**


# Challenges & Solutions


## Issue 1: Understanding the Task Background

**Solution:**  

Some confusion around:
Where to fetch crypto data from?
How to structure the project correctly?
How to integrate documentation with Docusaurus?

## Issue 2: "No QueryClient set" Error
**Problem:**  
React Query requires a `QueryClientProvider`.

**Solution:**  
Ensure `QueryClientProvider` wraps the entire app in `_app.tsx`:

```ts
import { QueryClient, QueryClientProvider } from "@tanstack/react-query";
const queryClient = new QueryClient();

return (
  <QueryClientProvider client={queryClient}>
    <Component {...pageProps} />
  </QueryClientProvider>
);
