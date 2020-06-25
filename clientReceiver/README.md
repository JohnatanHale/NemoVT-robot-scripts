# Salvataggio e condivisione dati

## Come Funziona
Si basa su MQTT, un protocollo TCP per lo scambio di dati che si distingue per non essere vincolato dalla rete.
Per avere accesso alla comunicazione bisogna possedere un certificato.

Il salvataggio di dati avviene dopo un breve periodo di tempo di raccolta dati.
1. Dopo aver ricevuto i dati, Halocode li invia tramite MQTT ad un topic, denominato "Topic Sensori"
2. Il client messo in ascolto allo stesso topic acquisisce i dati, successivamente inseriti in file .csv
3. Il dataset viene caricato su Google Drive automaticamente dal client

## Liberie usate
+ google-api-python-client
+ google-auth-oauthlib
+ tqdm
+ oauth2client
