# GroupMe Chat Exporter
<img width="796" height="462" alt="image" src="https://github.com/user-attachments/assets/455f93a3-7f48-4bd8-bbbc-53e283f5bcaa" />


A simple script to download your entire GroupMe chat history into a JSON file. It runs directly in your browser's developer console.

## Instructions

### 1. Get your Group ID
Log into GroupMe on the web (web.groupme.com) and open the chat you want to export. Look at the URL. It will look something like `web.groupme.com/groups/1234567`. Those numbers are your Group ID (Conversation ID).

<img width="455" height="32" alt="image" src="https://github.com/user-attachments/assets/0a1da849-20e4-4b0d-8e3a-8ad8fb35ac0c" />


### 2. Get your Access Token
1. Press `F12` to open Developer Tools.
2. Go to the **Network** tab.
3. Click anywhere in the chat or send a reaction to trigger a network request.
4. Look at the list of requests and click on one going to `api.groupme.com` (it might be named `messages`).
   <img width="826" height="349" alt="image" src="https://github.com/user-attachments/assets/56f9af63-ef4e-4239-983d-11ec0e8b1839" />
6. In the panel that opens, scroll down to the **Request Headers** section.
7. Find `X-Access-Token` and copy the long string of text next to it.

### 3. Add your info to the script
Open the script and put your Group ID and Access Token into the empty quotes at the very top:
`const GROUP_ID = "your_group_id_here";`
`const ACCESS_TOKEN = "your_token_here";`

### 4. Run it
1. In Developer Tools, switch over to the **Console** tab.
2. Paste your updated script into the console and press **Enter**.
3. The script will start pulling your messages. When it finishes reaching the beginning of the chat, it will automatically download a JSON file to your computer.
   <img width="790" height="415" alt="image" src="https://github.com/user-attachments/assets/27f7ce34-505f-435c-932e-91cfc8dfefc0" />
