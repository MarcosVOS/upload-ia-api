# upload-ia-api

### 🇺🇸 Project developed during RocketSeat's NLW Event to train integration with openAI with some modifications 

#### The project consists of an application where the user uploads a video and defines whether to generate suggestions for the title or description of the video, it also defines points such as temperature and key 

##### Technologies used: 
- NodeJS
- TypeScript 
- Prisma
- Fastify
- OpenAI
- Zod

  
##### Endpoints: 
###### http://localhost:8080/prompts
Returns the prompts registered in the database to generate the title or description 
###### http://localhost:8080/video
Upload the video and receive it via multipart/form-data
###### http://localhost:8080/videos/{video_id_replace}/transcription
Generates the video transcription, receives the video id via URL and a prompt via body of type application/json
``` 
  {
    "prompt":"texto"
  }
```
###### http://localhost:8080/prompts](http://localhost:8080/ai/complete)
Generates the summary, the requested prompt based on the requested value receives the following values ​​via body application/json: the videoId saved in the bank, temperature related to the creativity of the response and the prompt
``` 
  {
    "videoId":"video_id_replace",
    "temperature":0.5,
    "prompt":"prompt"
}
```





##### How to run:
``` 
pnpm i 
pnpm run dev
pnpm prisma studio // If you want to see the database
```
**If you want to execute and need to fill in the environment variables, there is an example file default.env**
[Link to the frontend](https://github.com/MarcosVOS/upload-ia-web)

___
### 🇧🇷 Projeto desenvolvido durante o Evento NLW da RocketSeact para treinar integração com a openAI com algumas modificações 

#### O projeto consiste em uma aplicação que o usuário faz o upload de um video e define se quer gerar sugestoes de título ou a descrição do video, também define pontos como a temperatura e palavras chaves 

##### Tecnologias usadas: 
- NodeJS
- TypeScript 
- Prisma
- Fastify
- OpenAI
- Zod

##### Endpoints: 
###### http://localhost:8080/prompts
Retorna os prompts cadastrados no banco para gerar o título ou a descrição 
###### http://localhost:8080/video
Faz o upload do video recebe por multipart/form-data
###### http://localhost:8080/videos/{Id_Do_Video_Subistituir}/transcription
Gera a transcrição do vídeo recebe por URL o id do video e um prompt por body do tipo application/json
``` 
  {
    "prompt":"texto"
  }
```
###### http://localhost:8080/prompts](http://localhost:8080/ai/complete
Gera o resumo o prompt solicitado com base no valor solicitado recebe por body application/json os seguintes valores: o videoId salvo no banco, temperatura relacionado a criatividade da resposta e o prompt  
``` 
  {
    "videoId":"Id_Do_Video_Subistituir",
    "temperature":0.5,
    "prompt":"prompt"
}
```



##### Como executar:
``` 
pnpm i 
pnpm run dev
pnpm prisma studio // Se você quiser ver o database
```
**Caso queira executar e necessário preencher as variaveis de ambiente existe um arquivo de exemplo default.env**
[Link para o frontend](https://github.com/MarcosVOS/upload-ia-web)
