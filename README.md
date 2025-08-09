# AI Agent with Tool Integration

An intelligent AI agent built with Google's Gemini AI that can perform various tasks using integrated tools. The agent can engage in natural conversation while having access to specialized functions for mathematical operations and cryptocurrency data retrieval.

## Features

- **Interactive Chat Interface**: Continuous conversation loop with the AI agent
- **Function Calling**: AI can automatically call appropriate tools based on user queries
- **Built-in Tools**:
  - **Sum Calculator**: Add two numbers together
  - **Prime Checker**: Determine if a number is prime
  - **Crypto Price Fetcher**: Get current cryptocurrency prices from CoinGecko API
- **Conversation History**: Maintains context throughout the session

## Prerequisites

- Node.js (version 14 or higher)
- npm or yarn package manager
- Google AI API key

## Installation

1. Clone or download this repository
2. Navigate to the project directory
3. Install dependencies:
   ```bash
   npm install
   ```

## Setup

1. Get a Google AI API key from [Google AI Studio](https://makersuite.google.com/app/apikey)
2. Replace the API key in `index.js` line 5:
   ```javascript
   const ai = new GoogleGenAI({ apiKey: "YOUR_API_KEY_HERE" });
   ```

## Usage

1. Start the application:
   ```bash
   node index.js
   ```

2. Enter your queries when prompted. The AI agent can:
   - Answer general questions directly
   - Perform calculations: "What's 15 + 27?"
   - Check prime numbers: "Is 17 a prime number?"
   - Get crypto prices: "What's the current price of bitcoin?"

3. Type your questions and press Enter. The agent will continue running until you exit with Ctrl+C.

## Example Interactions

```
Ask me anything--> What's 25 + 30?
55

Ask me anything--> Is 29 prime?
Yes, 29 is a prime number.

Ask me anything--> What's the price of ethereum?
[Returns current Ethereum price data]
```

## Available Tools

### Sum Calculator
- **Function**: `sum(num1, num2)`
- **Purpose**: Adds two numbers
- **Usage**: Ask questions like "What's X + Y?" or "Add 10 and 15"

### Prime Checker
- **Function**: `prime(num)`
- **Purpose**: Checks if a number is prime
- **Usage**: Ask "Is X prime?" or "Check if 23 is prime"

### Cryptocurrency Price Fetcher
- **Function**: `getCryptoPrice(coin)`
- **Purpose**: Fetches current crypto prices from CoinGecko
- **Usage**: Ask "What's the price of bitcoin?" or "Show me ethereum price"

## Dependencies

- `@google/genai`: Google's Generative AI SDK
- `readline-sync`: Synchronous readline for user input
- `i`: Utility package
- `npm`: Node package manager

## Project Structure

```
├── index.js          # Main application file
├── package.json      # Project dependencies and metadata
└── README.md         # Project documentation
```

## Security Note

⚠️ **Important**: Never commit API keys to version control. Consider using environment variables or a separate config file for sensitive data.

## Contributing

Feel free to add more tools or enhance the existing functionality. To add a new tool:

1. Create the function implementation
2. Define the function declaration schema
3. Add the function to the `availableTools` object
4. Include the declaration in the `functionDeclarations` array

## License

ISC License
