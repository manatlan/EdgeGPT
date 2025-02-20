<a id="EdgeGPT"></a>

# EdgeGPT

Main.py

<a id="EdgeGPT.Chatbot"></a>

## Chatbot Objects

```python
class Chatbot()
```

Combines everything to make it seamless

<a id="EdgeGPT.Chatbot.save_conversation"></a>

#### save\_conversation

```python
async def save_conversation(filename: str) -> None
```

Save the conversation to a file

<a id="EdgeGPT.Chatbot.load_conversation"></a>

#### load\_conversation

```python
async def load_conversation(filename: str) -> None
```

Load the conversation from a file

<a id="EdgeGPT.Chatbot.get_conversation"></a>

#### get\_conversation

```python
async def get_conversation() -> dict
```

Gets the conversation history from conversation_id (requires load_conversation)

<a id="EdgeGPT.Chatbot.ask"></a>

#### ask

```python
async def ask(
    prompt: str,
    wss_link: str = "wss://sydney.bing.com/sydney/ChatHub",
    conversation_style: CONVERSATION_STYLE_TYPE = None,
    webpage_context: str | None = None,
    search_result: bool = False,
    locale: str = guess_locale()) -> dict
```

Ask a question to the bot

<a id="EdgeGPT.Chatbot.ask_stream"></a>

#### ask\_stream

```python
async def ask_stream(
    prompt: str,
    wss_link: str = "wss://sydney.bing.com/sydney/ChatHub",
    conversation_style: CONVERSATION_STYLE_TYPE = None,
    raw: bool = False,
    webpage_context: str | None = None,
    search_result: bool = False,
    locale: str = guess_locale()
) -> Generator[bool, Union[dict, str], None]
```

Ask a question to the bot

<a id="EdgeGPT.Chatbot.close"></a>

#### close

```python
async def close() -> None
```

Close the connection

<a id="EdgeGPT.Chatbot.reset"></a>

#### reset

```python
async def reset() -> None
```

Reset the conversation

<a id="EdgeGPT.async_main"></a>

#### async\_main

```python
async def async_main(args: argparse.Namespace) -> None
```

Main function
