# Slackbot made by Jaram members
## Instuction
1. Get API key from Naver API portal. This API key should have access to Naver NMT API.   
2. Get API key from Slack.
3. Execute `EXPORT SLACKBOT_TOKEN=<Token from Slack>` to add SlackBot token to env vars.
4. Execute `EXPORT PAPAGO_CLIENT_ID=<Naver API Client ID>; EXPORT PAPAGO_CLIENT_SECRET=<Naver API Client Secret>` to add Papago API credentials to env vars.
    1. add lines above to shell rc files if you want to make this vars premanently.
5. Run `python3 main.py` to start bot.

## Usage 
- Movie Schedule: `영화`
     - If message is formatted properly, bot will send message which contains movie schedule of cinema near HYU@Erica.
     - Example: Sending `영화` will responded by message `*블랙 팬서* ...
        *조선명탐정: 흡혈괴마의 비밀* ...
        *골든슬럼버* ...
        *인시디어스4: 라스트 키* ...`
- Coinone Currency: `코인원 (빗코|비트코인|빗캐|이더|아이오타|...)`
     - If message is formatted properly, bot will send message which contains current coinone cryptocurrency currency(to KRW).
     - Check `CoinoneBot/cointickerbot.py` for all supported currencies.
     - Example: Sending `코인원 이더` will responded by message `2018-02-18 18:46:58 기준 가격 *KRW 1,040,100*`.
- Packt Ebook: `(eBook|ebook|Ebook|이북|e북)`
    - If message is formatted properly, bot will send message which contains title of today's Packt free eBook.
    - Example: Sending `eBook` will responded by message `AWS Administration - The Definitive Guide`.
- Github Stalking: `!github_(un)?register <UserID>`
    - If message is formatted properly, bot will inform you with confirmtion message.
    - Example: Sending `!github_register <UserId>` will responded by message `Registered user <UserID>`    
- Spell Check: `맞춤법:<Text>`
     - If message is formatted properly, bot will send message which contains message with fixed typos.
     - Example: Sending `맞춤법:외않되요` will responded by bot with message `왜 안 돼요`.
- Translator: `(한영|영한):<Text>`
     - If message is formatted properly, bot will send message which contains translated message of sent text.
     - Example: Sending `한영:안녕하세요` will responded by bot with message `Hello`.
