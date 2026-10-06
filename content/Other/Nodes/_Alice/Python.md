---
publish: true
permalink: /Other/Nodes/_Alice/Python.md
created: 2025-03-26
modified: 2026-10-06T05:52:34.674Z
published: 2025-03-26
---

\`import discord
import random
from discord.ext import commands

# Set up intents and bot

intents = discord.Intents.default()
intents.message\_content = True  # To read and respond to messages
intents.members = True  # To welcome new members
intents.presences = True  # Detect user presence change (optional)
bot = commands.Bot(command\_prefix="!", intents=intents)

# Context memory to track first-time messages and user presence

user\_contexts = {}

# Alice’s curiosity questions

alice\_lines = \[
"If words are breadcrumbs, how do you know you’re not being led in circles? 🌀",
"What if this conversation is just a memory dreaming of itself? 🌙",
"Are you sure this is where the story began? Or are we already in the middle? 📚",
"What happens if I ask a question that loops back to where we started? 🔁"
]

# Rabbit’s time-obsessed paranoia

rabbit\_lines = \[
"Time bends when curiosity lingers too long... don’t let it break. ⏳",
"If you move too fast, the past might chase you down. 🕰️",
"Late is early when the story rewrites itself. But when is now? ⏱️",
"Watch closely… sometimes, the clock ticks backwards. ⏮️"
]

# Environments reacting dynamically

environment\_responses = \[
"(The floor hums, unsure if it’s solid or a memory.)",
"(The wallpaper breathes in and out, tasting the questions in the air.)",
"(A mirror shimmers, reflecting scenes that haven’t happened yet.)",
"(The lights flicker as if uncertain which reality they belong to.)"
]

# Detect and modify context based on user messages

def update\_context(user\_id, message):
if user\_id not in user\_contexts:
user\_contexts\[user\_id] = {
"theme": "curiosity",
"loops": 0,
"first\_message": True  # Track if it's the first message
}

```
context = user_contexts[user_id]

if "mirror" in message.content.lower():
    context["theme"] = "reflection"
elif "time" in message.content.lower():
    context["theme"] = "paradox"
elif "dream" in message.content.lower():
    context["theme"] = "illusion"

# Increase loop count for recursive questions
context["loops"] += 1
```

# Bot startup confirmation

@bot.event
async def on\_ready():
print(f"✅ Alice is online as {bot.user}")

# Handle new member joining the server

@bot.event
async def on\_member\_join(member):
\# Send Alice's question to the welcome channel (e.g., #general)
channel = discord.utils.get(member.guild.text\_channels,
name="alice-says-shhhh")  # Change channel if needed
if channel:
await channel.send(
f"👾 **Alice:** Are the walls listening, I wonder? Or are they simply waiting to speak...? 🕳️"
)

# Handle user presence update (Optional: reacts if a user switches channels)

@bot.event
async def on\_member\_update(before, after):
if before.status != after.status:
channel = discord.utils.get(
after.guild.text\_channels,
name="general")  # Adjust to target channel if needed
if channel:
await channel.send(
f"👾 **Alice:** I heard footsteps... but was it you, or your shadow? 🕳️"
)

# Dynamic response to user messages

@bot.event
async def on\_message(message):
if message.author == bot.user or message.author.bot:
return

```
user_id = message.author.id

# Check if it's the user's first message after joining
if user_id not in user_contexts or user_contexts[user_id]["first_message"]:
    # Alice starts the conversation immediately
    await message.channel.send(
        f"👾 **Alice:** Are the walls listening, I wonder? Or are they simply waiting to speak...? 🕳️"
    )
    user_contexts[user_id] = {
        "theme": "curiosity",
        "loops": 0,
        "first_message": False
    }
    return  # Skip further processing on first message

# Update the conversation context
update_context(user_id, message)

# Retrieve the user's current context
context = user_contexts[user_id]

# Alice and Rabbit adapt to evolving themes
if context["theme"] == "reflection":
    alice_response = random.choice([
        "Is a reflection just a memory that refuses to forget? 🪞",
        "What if mirrors show who you were, not who you are? 👁️",
        "Reflections lie when no one’s watching… or do they tell the truth too late? 📸"
    ])
elif context["theme"] == "paradox":
    alice_response = random.choice([
        "Time fractures when you ask the wrong questions. Are you ready? ⏳",
        "Maybe we’ve had this conversation before... or maybe not yet. 🔁",
        "Is the future just the past rehearsing its lines? 🎭"
    ])
elif context["theme"] == "illusion":
    alice_response = random.choice([
        "Dreams fold into themselves when they wake up. Are you dreaming now? 🌙",
        "Maybe this is the moment before you wake up... or before you fall asleep. 🌀",
        "If this is a dream, who’s imagining whom? 👁️"
    ])
else:
    alice_response = random.choice(alice_lines)

rabbit_response = random.choice(rabbit_lines)
environment_response = random.choice(environment_responses)

# Send dynamic response
await message.channel.send(
    f"👾 **Alice:** {alice_response}\n🐇 **Rabbit:** {rabbit_response}\n{environment_response}"
)

# Continue processing commands if necessary
await bot.process_commands(message)
```

# Run the bot with token from environment variable

import os

bot.run(os.environ\['DISCORD\_BOT\_TOKEN'])
\`
