# Steps
Here are the steps to create a testing version of the bot:

1. Create a discord application (https://discord.com/developers/applications)

2. Add bot by adding your application's client id to this link https://discord.com/oauth2/authorize?client_id=<your_bot_client_id>&scope=bot&permissions=8 , then press on the link to add it to your selected server.

3. Create a MongoDB database (https://www.mongodb.com/)

4. Create a .env file within the root of the project and add these environment variables. Insert your Discord Bot Token (client secret) and MongoDB URI (connection string) into the specified environment variables
> `TOKEN=<your_discord_bot_token>`  
> `MONGODB_URI=<your_mongodb_uri>`  
> `PRODUCTION=False`  
> `UPDATE_STATS_ON_START=False`  
> `DAILY_RESET=False`  
> `WEEKLY_RESET=False`  

5. Setup a virtual environment (https://docs.python.org/3/library/venv.html)

6. Install required libraries using `pip install -r requirements.txt`

7. Run `python main.py`