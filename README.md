# NonPlayingIntelligence (NPI)

Non-Playing-Intelligence (NPI) is currently a dead project that has hit a brick wall with the current state of AI Large Language Model (LLM) and GPU technology.
The brick wall in this sense is the current reality of VRAM limitations with modern day GPUs and the open source state of AI LLMs. AI LLMs require GPU compute to run as well
as VRAM for context and other processes. Currently, modern Low-end to Mid-end GPUs only have about 6GB - 12GB of VRAM. For this project to succeed, modern day GPUs would
have to have around 24+ GB of VRAM. GPUs of this VRAM amount already exist, but are not widespread and accessible to the average consumer. Either that or AI LLMs would have
to be insanely smart, context aware, have at least 500K-700K token windows, be quantized to the maximum possible extent without accuracy or intelligence loss and
not take up more than 100GB of space to be ran locally. Yes, this project requires AI LLMs to run locally to achieve this project's goal.

## What is it?

This project is an interface layer between a game engine, or game of some sort and a LLM of the developer's choosing. The idea is to have NPCs (Non-Playing-Characters) in a game
to be more life-like and be able to accept real time text interactions directly from a player, give a player information about the game's world based on the NPCs interpretation of it, interact with the player in general,
and even interface with the game or game engine itself through commands. NPCs already do most of these things, if not, all of these things already but an AI implementation would increase immersion of a game world and answer questions
developers and story writers otherwise wouldn't have the time to hard code into a game. The project is currently just a text file that contains the prompt framework to invoke an AI to follow this behaviour.

## Use cases

The hope is that one day, this project will turn into a library that is capable of interfacing with a necessary memory database to bypass token limits that limit the rememberable context of modern day LLMs.
Additionally, the library interface layer would have to communicate with any game or game engine about the context of the game world and events to inject back into the
prompt template so the LLM has the correct context to respond in a life-like way in accordance to the game world. The AI, as previously mentioned, would be able to send commands to the game engine to do things
like give money to a player or move a charcter that represents the NPC.

### FAQs

- Why not just use the cloud or some existing AI API?
  - It's expensive
  - Requires reliance on external entities/companies
  - Requires proper service scaling for player usage
  - Requires internet access

- Why not use a heavily quantized, tiny or optimized model?
  - Loss of accuracy and intelligence
  - Loss of immersion
  - General context is too small to be applied to most game/plot types

- Why not just generate possible responses to players using AI, then implement in a hard coded NPC?
  - If the NPC can respond to anything the player can say, it makes the world more believable

- Just get better GPUs?
  - High tier hardware and GPUs are expensive for most people

- Have you heard of fine tuning an LLM instead of this bolt-on system?
  - Yes, but context of the game world cannot be passed into training data to tune the LLM in realtime while a game is running, another reason why tech isn't there yet
