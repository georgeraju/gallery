# technews_summary Skill

## Skill Definition
The `technews_summary` skill is designed to fetch the latest technology news from the newsdata.io API and summarize it for quick consumption. This skill helps users stay updated with the most recent developments in the tech industry, providing a concise overview of trending stories.

## Instructions for Fetching Tech News

1. **API Key**: To use the newsdata.io API, you need to sign up at [newsdata.io](https://newsdata.io) and obtain your unique API key.
  
2. **Endpoint**:
   The primary endpoint for fetching technology news is:
   ```
   https://newsdata.io/api/1/news
   ```

3. **Parameters**:
   - `apikey`: Your API key.
   - `category`: Set this to `technology` to fetch tech news.
   - `language`: Specify the language of the articles you want to retrieve (e.g., `en` for English).
   - Additional parameters can be included to filter by domain, country, etc.

4. **Example Request**:
   A sample GET request to fetch technology news could look like this:
   ```
   GET https://newsdata.io/api/1/news?apikey=YOUR_API_KEY&category=technology&language=en
   ```

5. **Response Structure**:
   The API will return a JSON response containing the news articles. Each article typically includes fields like `title`, `description`, `link`, `pubDate`, and more.

6. **Usage**:
   Integrate the API call in your skill to process fetched articles. You may want to select the top articles and format them into a summary for the user.

## Example Code Snippet
```python
import requests

def fetch_tech_news(api_key):
    url = "https://newsdata.io/api/1/news"
    params = {
        'apikey': api_key,
        'category': 'technology',
        'language': 'en'
    }
    
    response = requests.get(url, params=params)
    data = response.json()
    
    return data.get('articles', [])
```

Make sure to replace `YOUR_API_KEY` with your actual key in the example request and integrate the example code into your skill's functionality to fetch and display tech news.
