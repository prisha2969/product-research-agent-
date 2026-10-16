# 🛒 Product Research Agent (n8n + Gemini + Firecrawl)

An AI agent that researches any commercial product and generates a
market report: price range, top 3 comparison, common complaints,
and a buy/sell recommendation.

![Product Research Agent workflow](workflow.png)

## How it works
1. User sends a product query in the n8n chat
2. Agent searches review/comparison articles via Firecrawl Search
3. Scrapes the top 2 results via Firecrawl Scrape
4. Gemini analyses the data and returns a structured report

## Tech stack
- n8n (workflow automation)
- Google Gemini Chat Model
- Firecrawl (search + scrape)
- Simple Memory (conversation context)

## Setup
1. Import `workflow.json` into n8n (Workflows → Import from file)
2. Add your credentials: Google Gemini API key, Firecrawl API key
3. Paste the prompt from `system-prompt.md` into the AI Agent's System Message
4. Open the chat and try: "best wireless earbuds under ₹2000"

## Example output
![Chat demo](images/chat-demo.png)
**Query:** `Best air fryer in Egypt EGP`
<details> <summary>Click to view the full report</summary>
📊 **MARKET OVERVIEW**
-	**Number of products found: ** 50+ models across major retailers.
-	**Price range: ** 1,499 EGP – 8,900 EGP.
-	**Average rating: **4.3 / 5 stars.


## Limitations
- Depends on the quality of the review pages found
- Prices can be outdated, so check the source link

