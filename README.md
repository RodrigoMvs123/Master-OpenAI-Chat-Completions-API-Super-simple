
## Master-OpenAI-Chat-Completions-API-Super-simple

https://www.youtube.com/watch?v=fSFJrG1wwm8 

https://raw.githubusercontent.com/RodrigoMvs123/Master-OpenAI-Chat-Completions-API-Super-simple/main/README.md

https://github.com/RodrigoMvs123/Master-OpenAI-Chat-Completions-API-Super-simple/blame/main/README.md

## OpenAi

Docs

https://platform.openai.com/docs/introduction 

Text Generation
https://platform.openai.com/docs/guides/text-generation 

Chat Completions 
https://platform.openai.com/docs/guides/text-generation/chat-completions-api 


## Create React App

```bash
  npx create-react-app openai-chat-completions-demo
```

### Visual Studio Code
Terminal
```bash
npx create-react-app openai-chat-completions-demo
```

## Source Code

```javascript
Visual Studio Code
Explorer
Open Editors
App.js

App.js
const App = () => {
  return (
    <div></div>
  )
}

export default App;
```

```javascript
Visual Studio Code
Explorer 
Open Editors
App.js
index.js

index.js
import React from 'react'
import ReactDOM from 'react-dom/client'
import App from './App'

const root = ReactDOM.createRoot(document.getElementById('root'))
root.render(
  <React.StrictMode>
    <App />
  </React.StrictMode>
)
```

```javascript
Visual Studio Code
Explorer 
Open Editors
App.js
index.js
server.js

server.js
import OpenAI from "openai"

const openai = new OpenAI()

async function main() {
  const completion = await openai.chat.completions.create({
    messages: [{"role": "system", "content": "You are a helpful assistant."},
        {"role": "user", "content": "Who won the world series in 2020?"},
        {"role": "assistant", "content": "The Los Angeles Dodgers won the World Series in 2020."},
        {"role": "user", "content": "Where was it played?"}],
    model: "gpt-3.5-turbo",
  });

  console.log(completion.choices[0]) 	
}
main()
```

## OpenAI API Key
```bash
my-demo
apiKey: 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
```

## Source Code
```javascript
Visual Studio Code
Explorer
Open Editors
App.js
index.js
server.js

server.js
import OpenAI from "openai"

const openai = new OpenAI({ apiKey: process.env.OPENAI_API_KEY })

async function main() {
  const completion = await openai.chat.completions.create({
    messages: [{"role": "system", "content": "You are a helpful assistant."},
        {"role": "user", "content": "Who won the world series in 2020?"},
        {"role": "assistant", "content": "The Los Angeles Dodgers won the World Series in 2020."},
        {"role": "user", "content": "Where was it played?"}],
    model: "gpt-3.5-turbo",
  });

  console.log(completion.choices[0])
}
main()
```

```javascript
Visual Studio Code
Explorer
Open Editors
App.js
index.js
server.js
.env

.env
OPENAI_API_KEY=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
```

### Visual Studio Code
Terminal
```bash
npm i dotenv
```

## Source Code
```javascript
Visual Studio Code
Explorer
Open Editors
App.js
index.js
server.js
.env

server.js
const OpenAI = require("openai")
require('dotenv').config()

const openai = new OpenAI({ apiKey: process.env.OPENAI_API_KEY })

async function main() {
  const completion = await openai.chat.completions.create({
    messages: [{"role": "system", "content": "You are a helpful assistant."},
        {"role": "user", "content": "Who won the world series in 2020?"},
        {"role": "assistant", "content": "The Los Angeles Dodgers won the World Series in 2020."},
        {"role": "user", "content": "Where was it played?"}],
    model: "gpt-3.5-turbo",
  });

  console.log(completion.choices[0])
}
main()
```

```javascript
Visual Studio Code
Explorer
Open Editors
App.js
index.js
server.js
.env
package.json

package.json
"scripts": {
  "start:frontend": "react-scripts start",
  "start:backend": "nodemon server.js",
  "build": "react-scripts build",
  "test": "react-scripts test",
  "eject": "react-scripts eject"
}
```

### Visual Studio Code
Terminal
```bash
npm i nodemon
```

## Source Code
```javascript
Visual Studio Code
Explorer
Open Editors
App.js
index.js
server.js
.env
package.json

package.json
{
  "dotenv": "^16..4.5",
  "nodemon": "^3.1.0"
}
```

### Visual Studio Code
Terminal
```bash
npm i openai
```
## Source Code

```javascript
Visual Studio Code
Explorer
Open Editors
App.js
index.js
server.js
.env
package.json

package.json
{
  "dotenv": "^16..4.5",
  "nodemon": "^3.1.0",
  "openai": "^4.29.2"
}
```

### Visual Studio Code
Terminal
```bash
npm run start:backend
```

## Source Code

```javascript
Visual Studio Code
Explorer
Open Editors
App.js
index.js
server.js
.env
package.json

server.js
const PORT = 8000 
const express = require('express')
const cors = require('cors')
const app = express()
const OpenAI = require("openai")
require('dotenv').config()

app.use(express.json())
app.use(cors())

const openai = new OpenAI({ apiKey: process.env.OPENAI_API_KEY })

async function main() {
  const completion = await openai.chat.completions.create({
    messages: [{"role": "system", "content": "You are a helpful assistant."},
        {"role": "user", "content": "Who won the world series in 2020?"},
        {"role": "assistant", "content": "The Los Angeles Dodgers won the World Series in 2020."},
        {"role": "user", "content": "Where was it played?"}],
    model: "gpt-3.5-turbo",
  });

  console.log(completion.choices[0])
}
main()
```

### Visual Studio Code
Terminal
```bash
npm i express cors
```

```javascript
Visual Studio Code
Explorer
Open Editors
App.js
index.js
server.js
.env
package.json

package.json
{
  "dependencies": {
    "dotenv": "^16.4.5"
  }
}
"scripts": {
  "start:frontend": "react-scripts start",
  "start:backend": "nodemon server.js",
  "build": "react-scripts build",
  "test": "react-scripts test",
  "eject": "react-scripts eject"
}
{
  "cors": "^2.8.5",
  "dotenv": "^16..4.5",
  "express": "^4.19.2",
  "nodemon": "^3.1.0",
  "openai": "^4.29.2"
}
```

```javascript
Visual Studio Code
Explorer
Open Editors
App.js
index.js
server.js
.env
package.json

server.js
const PORT = 8000 
const express = require('express')
const cors = require('cors')
const app = express()
const OpenAI = require("openai")
require('dotenv').config()

app.use(express.json())
app.use(cors())

const openai = new OpenAI({ apiKey: process.env.OPENAI_API_KEY })

app.post('/completion', async (req, res) => {
  const text = req.body.text
  const completion = await openai.chat.completions.create({
    messages: [{"role": "system", "content": "You are a helpful assistant."},
        {"role": "user", "content": text}
      ],
    model: "gpt-3.5-turbo",
  });
  console.log(completion.choices[0])
})

app.listen(PORT, () => console.log(`Listening on port ${PORT}!`))
```

### Visual Studio Code
Terminal
```bash
npm run start:frontend
```

## localhost:3000 

```javascript
Visual Studio Code
Explorer
Open Editors
App.js
index.js
server.js
.env
package.json

App.js
import { useState } from "react"

const App = () => {
  const [ text, setText] = useState('')

  console.log(text)

  return (
    <div>
      <input onChange={e => setText(e.target.value)}/>
      <button>Submit</button>
      <p></p>
    </div>
  )
}

export default App;
```

## localhost:3000
[                       ] Submit 

## Source Code
```javascript
Visual Studio Code
Explorer
Open Editors
App.js
index.js
server.js
.env
package.json

App.js
import { useState } from "react"

const App = () => {
  const [ text, setText] = useState('')

  const getCompletion = async() => {
    const response = await fetch('http://localhost:8000/completion', {
      method: 'POST',
      body: JSON.stringify({text}),
      headers: {'Content-Type': 'application/json'}
    })
    const data = await response.json()
    console.log(data)
  }

  return (
    <div>
      <input onChange={e => setText(e.target.value)}/>
      <button onClick={getCompletion}>Submit</button>
      <p></p>
    </div>
  )
}

export default App;
```

## localhost:8000
[ What day is it ] Submit

### Visual Studio Code
Terminal

Listening on port 8000!
```bash
{
	index: 0,
	message: {
		role: ‘assistant’,
		content: ‘Today is Tuesday, how can I assist you today?’
},
```

## Source Code
```javascript
Visual Studio Code
Explorer
Open Editors
App.js
index.js
server.js
.env
package.json

server.js
const PORT = 8000 
const express = require('express')
const cors = require('cors')
const app = express()
const OpenAI = require("openai")
require('dotenv').config()

app.use(express.json())
app.use(cors())

const openai = new OpenAI({ apiKey: process.env.OPENAI_API_KEY })

app.post('/completion', async (req, res) => {
  const text = req.body.text
  const completion = await openai.chat.completions.create({
    messages: [{"role": "system", "content": "You are a helpful assistant."},
        {"role": "user", "content": text}
      ],
    model: "gpt-3.5-turbo",
  });
  console.log(completion.choices[0])
  res.send(completion.choises[0])
})

app.listen(PORT, () => console.log(`Listening on port ${PORT}!`))
```

## localhost:8000
[ What day is it ] Submit

### Visual Studio Code
Terminal

Listening on port 8000!

Console
```bash
{ index: 0, message: {...}, logprobs: null, finish_reason: ‘stop’ }
	finish_reason: “stop”
	index: 0
	logprobs: null
	message: 
		content: “Today is Saturday”
		role: “assistant”
		[[Prototype]]: Object
	         [[Prototype]]: Object
```

## Source Code
```javascript
Visual Studio Code
Explorer
Open Editors
App.js
index.js
server.js
.env
package.json

App.js
import { useState } from "react"

const App = () => {
  const [ text, setText] = useState('')
  const [ response, setResponse] = useState('')

  const getCompletion = async() => {
    const response = await fetch('http://localhost:8000/completion', {
      method: 'POST',
      body: JSON.stringify({text}),
      headers: {'Content-Type': 'application/json'}
    })
    const data = await response.json()
    console.log(data)
    setResponse(data.message.content)
  }

  return (
    <div>
      <input onChange={e => setText(e.target.value)}/>
      <button onClick={getCompletion}>Submit</button>
      <p>{response}</p>
    </div>
  )
}

export default App;
```

## localhost:8000
[ What day is it ] Submit

Today is Friday.

## Source Code
```javascript
Visual Studio Code
Explorer
Open Editors
App.js
index.js
server.js
.env
package.json

server.js
const PORT = 8000 
const express = require('express')
const cors = require('cors')
const app = express()
const OpenAI = require("openai")
require('dotenv').config()

app.use(express.json())
app.use(cors())

const openai = new OpenAI({ apiKey: process.env.OPENAI_API_KEY })

app.post('/completion', async (req, res) => {
  const text = req.body.text
  const completion = await openai.chat.completions.create({
    messages: [{"role": "system", "content": "You are a helpful assistant."},
        {"role": "user", "content": text}
      ],
    model: "gpt-3.5-turbo",
  });
  console.log(completion)
  // res.send(completion.choises[0])
})

app.listen(PORT, () => console.log(`Listening on port ${PORT}!`))
```

### Visual Studio Code
Terminal

Listening on port 8000!
```bash
{
	id:
	object:
	created:
	model:
	choices: [
		{
			index:
			message:
			logoprobs:
			finish_reason:
		}
],
```

## Source Code
```javascript
Visual Studio Code
Explorer
Open Editors
App.js
index.js
server.js
.env
package.json

App.js
import { useState } from "react"

const App = () => {
  const [ text, setText] = useState('')
  const [ response, setResponse] = useState('')

  const getCompletion = async() => {
    const response = await fetch('http://localhost:8000/completion', {
      method: 'POST',
      body: JSON.stringify({text}),
      headers: {'Content-Type': 'application/json'}
    })
    const data = await response.json()
    console.log(data)
    setResponse(data.message.content)
  }

  return (
    <div>
      <input onChange={e => setText(e.target.value)}/>
      <button onClick={getCompletion}>Submit</button>
      <p>{response}</p>
    </div>
  )
}

export default App;
```

## localhost:8000

[ What day is it ] Submit

Today is Friday.

## Source Code
```javascript
Visual Studio Code
Explorer
Open Editors
App.js
index.js
server.js
.env
package.json

App.js
import { useState } from "react"

const App = () => {
  const [ text, setText] = useState('')
  const [ response, setResponse] = useState('')

  const getCompletion = async() => {
    const response = await fetch('http://localhost:8000/completion', {
      method: 'POST',
      body: JSON.stringify({text}),
      headers: {'Content-Type': 'application/json'}
    })
    const data = await response.json()
    setResponse(data.message.content)
  }

  return (
    <div>
      <input onChange={e => setText(e.target.value)}/>
      <button onClick={getCompletion}>Submit</button>
      <p>{response}</p>
    </div>
  )
}

export default App;
```
