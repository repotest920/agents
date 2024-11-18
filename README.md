<!--BEGIN_BANNER_IMAGE-->

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="/.github/banner_dark.png">
  <source media="(prefers-color-scheme: light)" srcset="/.github/banner_light.png">
  <img style="width:100%;" alt="The LiveKit icon, the name of the repository and some sample code in the background." src="https://raw.githubusercontent.com/livekit/agents/main/.github/banner_light.png">
</picture>

<!--END_BANNER_IMAGE-->

<!--BEGIN_DESCRIPTION-->
<br /><br />
Looking for the JS/TS library? Check out [AgentsJS](https://github.com/livekit/agents-js)

## ✨ [NEW] OpenAI Realtime API support

We are partnering with OpenAI on a new `MultimodalAgent` API in the Agents framework. This class completely wraps OpenAI’s Realtime API, abstracts away the raw wire protocol, and provide an ultra-low latency WebRTC transport between GPT-4o and your users’ devices. This same stack powers Advanced Voice in the ChatGPT app.

- Try the Realtime API in our [playground](https://playground.livekit.io/) [[code](https://github.com/livekit-examples/realtime-playground)]
- Check out our [guide](https://docs.livekit.io/agents/openai) to building your first app with this new API

## What is Agents?

The Agents framework allows you to build AI-driven server programs that can see, hear, and speak in realtime. Your agent connects with end user devices through a LiveKit session. During that session, your agent can process text, audio, images, or video streaming from a user's device, and have an AI model generate any combination of those same modalities as output, and stream them back to the user. 

## Features

- Plugins for popular LLMs, transcription and text-to-speech services, and RAG databases
- High-level abstractions for building voice agents or assistants with automatic turn detection, interruption handling, function calling, and transcriptions
- Compatible with LiveKit's [telephony stack](https://github.com/livekit/sip), allowing your agent to make calls to or receive calls from phones
- Integrated load balancing system that manages pools of agents with edge-based dispatch, monitoring, and transparent failover
- Running your agents is identical across localhost, [self-hosted](https://github.com/livekit/livekit), and [LiveKit Cloud](https://cloud.livekit.io) environments

<!--END_DESCRIPTION-->

## Installation

To install the core Agents library:

```bash
pip install livekit-agents
```

## Plugins

The framework includes a variety of plugins that make it easy to process streaming input or generate output. For example, there are plugins for converting text-to-speech or running inference with popular LLMs. Here's how you can install a plugin:

```bash
pip install livekit-plugins-openai
```

The following plugins are available today:

| Plugin                                                                             | Features                                    |
| ---------------------------------------------------------------------------------- | ------------------------------------------- |
| [livekit-plugins-anthropic](https://pypi.org/project/livekit-plugins-anthropic/)   | LLM                                         |
| [livekit-plugins-assemblyai](https://pypi.org/project/livekit-plugins-assemblyai/) | STT                                         |
| [livekit-plugins-azure](https://pypi.org/project/livekit-plugins-azure/)           | STT, TTS                                    |
| [livekit-plugins-deepgram](https://pypi.org/project/livekit-plugins-deepgram/)     | STT                                         |
| [livekit-plugins-cartesia](https://pypi.org/project/livekit-plugins-cartesia/)     | TTS                                         |
| [livekit-plugins-elevenlabs](https://pypi.org/project/livekit-plugins-elevenlabs/) | TTS                                         |
| [livekit-plugins-playht](https://pypi.org/project/livekit-plugins-playht/)         | TTS                                         |
| [livekit-plugins-google](https://pypi.org/project/livekit-plugins-google/)         | STT, TTS                                    |
| [livekit-plugins-nltk](https://pypi.org/project/livekit-plugins-nltk/)             | Utilities for working with text             |
| [livekit-plugins-rag](https://pypi.org/project/livekit-plugins-rag/)               | Utilities for performing RAG                |
| [livekit-plugins-openai](https://pypi.org/project/livekit-plugins-openai/)         | LLM, STT, TTS, Assistants API, Realtime API |
| [livekit-plugins-silero](https://pypi.org/project/livekit-plugins-silero/)         | VAD                                         |

## Documentation and guides

Documentation on the framework and how to use it can be found [here](https://docs.livekit.io/agents)

## Example agents

| Description                                                                                                   | Demo Link                                       | Code Link                                                                                      |
|---------------------------------------------------------------------------------------------------------------|-------------------------------------------------|-----------------------------------------------------------------------------------------------|
| A basic voice agent using a pipeline of STT, LLM, and TTS                                                     | [demo](https://kitt.livekit.io)                 | [code](https://github.com/livekit/agents/blob/main/examples/voice-pipeline-agent/minimal_assistant.py)  |
| Voice agent using the new OpenAI Realtime API                                                                 | [demo](https://playground.livekit.io)           | [code](https://github.com/livekit-examples/realtime-playground)                                        |
| Super fast voice agent using Cerebras hosted Llama 3.1                                                        | [demo](https://cerebras.vercel.app)             | [code](https://github.com/dsa/fast-voice-assistant/)                                                     |
| Voice agent using Cartesia's Sonic model                                                                      | [demo](https://cartesia-assistant.vercel.app/)  | N/A                                                                                           |
| Agent that looks up the current weather via function call                                                     | N/A                                             | [code](https://github.com/livekit/agents/blob/main/examples/voice-pipeline-agent/function_calling_weather.py)  |
| Voice agent that performs a RAG-based lookup                                                                  | N/A                                             | [code](https://github.com/livekit/agents/tree/main/examples/voice-pipeline-agent/simple-rag)           |
| Video agent that publishes a stream of RGB frames                                                             | N/A                                             | [code](https://github.com/livekit/agents/tree/main/examples/simple-color)                         |
| Transcription agent that generates text captions from a user's speech                                         | N/A                                             | [code](https://github.com/livekit/agents/tree/main/examples/speech-to-text)                        |
| A chat agent you can text who will respond back with generated speech                                          | N/A                                             | [code](https://github.com/livekit/agents/tree/main/examples/text-to-speech)                       |
| Localhost multi-agent conference call                                                                         | N/A                                             | [code](https://github.com/dsa/multi-agent-meeting)                                                |
| Moderation agent that uses Hive to detect spam/abusive video                                                  | N/A                                             | [code](https://github.com/dsa/livekit-agents/tree/main/hive-moderation-agent)                     |


