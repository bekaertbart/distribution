# distribution

I use this repository to distribute the applications I developed.

So far only the Twitchconsole. Make sure all settings are valid in the config file before starting.

# twitchconsole

A Twitch bot to say hi when someone speaks for the first time since application startup


Add to appsettings to set options:

<table>
	<tr>
		<th>key</th>
		<th>value</th>
	</tr>
	<tr>
		<td>username</td>
		<td>username to use in chat when sending message</td>
	</tr>	
	<tr>
		<td>streamer</td>
		<td>channel to monitor and chat in</td>
	</tr>
	<tr>
		<td>oauth</td>
		<td>get chat bot's oauth from www.twitchapps.com/tmi/ Make sure the token belongs to the given username</td>
	</tr>
	<tr>
		<td>exclude</td>
		<td>comma seperated usernames to exclude from greetings. Streamer and username are excluded automatically.</td>
	</tr>
	<tr>
		<td>greeting</td>
		<td>message to send to chat when a user comments for the first time ($user$ gets replaced with user chatting)</td>
	</tr>
	<tr>
		<td>delay</td>
		<td>delay to send messages in seconds</td>
	</tr>
	<tr>
		<td>timerCommand</td>
		<td>text to be sent on timer elapse</td>
	</tr>
	<tr>
		<td>timerPeriod</td>
		<td>time in seconds to send timerCommand</td>
	</tr>
</table>

These are read once upon start of application

# version history

<table>
	<tr>
		<td>
			1.3
		</td>
		<td>
			<ul><li>Added a timer sending text at set interval if file "command.yes" exists. Rename to keep the command from being sent</li><li>Chatlog is now saved in daily files (as opposed to one file per streamer)</li></ul>
		</td>
	</tr>
	<tr>
		<td>
			1.2
		</td>
		<td>
			<ul><li>At start, read the log of today and add those to the greeted chatters</li></ul>
		</td>
	</tr>
	<tr>
		<td>
			1.1
		</td>
		<td>
			<ul><li>Added a daily log with users that were greeted</li></ul>
		</td>
	</tr>
	<tr>
		<td>
			1.0
		</td>
		<td>
			First version
			<ul> 
				<li>Connects to Twitch IRC chat, using username and OAuth token</li>
				<li>Sends a greeting to users that say something in chat for the first time</li>
				<li>Using settings in config file</li>
			</ul>
		</td>
	</tr>
</table>