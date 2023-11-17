# ChatGPT_Trading_Bot

The ChatGPT trading bot project combines OpenAI's ChatGPT, known for its natural language processing, with a trading bot for financial markets. Users interact with the bot through conversational input, seeking market insights, making trading decisions, or receiving analysis in a user-friendly, chat-based interface. Leveraging ChatGPT's language capabilities, the system interprets user instructions and provides responses, enhancing the overall user experience. The project aims to streamline communication between traders and automated trading systems, making it more accessible and intuitive. As with any AI-driven trading system, careful attention is given to ethical considerations, legal compliance, and risk management practices. Users should refer to official project documentation for the latest information and updates.

* Pull 30 days of trading data for (Insert your stock or crypto) with Yahoo Finance Downloader API
* Create a simulated trading environment using real trading data with FinRL
* Train an neural network to predict that Stock Price using reinforcement learning inside this simulation with FinRL
* Once trained, backtest the predictions on the past 30 days data to compute potential returns with FinRL
* If the expectd returns are above a certain threshold, buy, else hold. If they're below a certain threshold, sell. (using Alpaca API)

<img src="https://camo.githubusercontent.com/b0ebbb985cd4de4f5944305231d225d512cdee29d35448cb1a3b18a1b82dfd59/68747470733a2f2f692e6962622e636f2f344b4a783979302f53637265656e2d53686f742d323032332d30312d31332d61742d31302d30342d33392d414d2e706e67" alt="alt text" data-canonical-src="https://i.ibb.co/4KJx9y0/Screen-Shot-2023-01-13-at-10-04-39-AM.png" style="max-width: 100%;">
# Dependencies
* **Python 3.7**
* **Alpaca SDK**
* **FinRL**
* **Vercel**
* **Firebase Template optional**

# Setup Instructions
*  Download the iPython notebook in this repository and upload it to Colab to try it out.
* Setup a simple flask app.
* To set up a cron job for a Flask app deployed on Vercel that executes a Google Colab notebook at a given link every hour, you can use the built-in Vercel cron feature. Here are the steps to follow:
* In your Flask app, import the necessary modules to run the Colab notebook, such as gdown or pyngrok
* Create a new endpoint in your Flask app that triggers the execution of the Colab notebook, using the link to the notebook file.
* Go to the Vercel project settings for your app and navigate to the "Cron" tab.
* Create a new cron job that runs every hour by adding the endpoint you created in step 2 to the "Cron Job" field and select the frequency you want to run the job.

Here is a sample code snippet for step 2:


> from flask import Flask, jsonify
> import gdown
> app = Flask(__name__)

> @app.route('/run-colab')
> def run_colab():
  >  gdown.download('https://.............<colab_notebook_id>', 'colab.ipynb', quiet=False)
   > return jsonify(message='colab notebook ran successfully')

# Credits & More Resources
Credits for the notebook go to the AI4FinanceFoundation, and for the API go to Alpaca.
