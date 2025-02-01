# 1. SERVER CURRENCIES!!

 ## 1. Botcoin
 ***Earning Method:*** Botcoin can be earned through participation in server activities:
 - Daily Quests: Implement daily tasks like collecting specific resources, defeating mobs, or completing mini-games. Use a plugin like "Quests" or "BetonQuest" to manage these.
 - Weekly Quests: Similar to daily quests but with more challenging or time-consuming tasks, perhaps involving community projects or server-wide events.
 
 ## 2. CosmeticCoin
 ***Conversion:*** Players can convert Botcoin into CosmeticCoin at a predefined rate (e.g., 1 Botcoin = 10 CosmeticCoins) through the Datorium bot:
 __**This conversion should be managed externally via Discord to avoid any direct in-game transaction of Botcoin.**__
 ***Usage:*** 
 CosmeticCoin is used to purchase cosmetic items or ranks:
 ***Ranks:***
  Cosmetic ranks like "MVP" that offer unique chat colors, titles, or special visual effects in certain server areas. Use a permission management plugin like "LuckPerms" to handle these ranks.
 ***Cosmetic Items:***
 Could include custom skins, capes, or other non-gameplay affecting items. Ensure these are managed through a cosmetic shop plugin or custom commands.
 
 ## 3. ServerCoin
 ***Earning Method:*** 
 ServerCoin can be earned through in-game activities or could be awarded for server participation, like voting for the server, participating in events, or through in-game economy plugins that reward players for game play (e.g., selling items to the server shop or through trading).
 ***Usage:*** ServerCoin is used for purchasing server-specific items:
 - Blocks: Decorative blocks, Ore blocks, Building blocks.
 - Enchantments: Unique or enhanced enchantments for tools, weapons, or armor.
 - Other Items: Could include server-specific tools, decorative items, or temporary boosts like speed or jump height.
 
 ## Integration and Display:
 ***In-Game Display:*** Players will see their CosmeticCoin and ServerCoin balances displayed on their screen at all times:
 Use a plugin like "**PlaceholderAPI**" along with "**HolographicDisplays**" or "**ScoreboardStats**" to display these values. Ensure the display is clear and non-intrusive.
 Settings Command: Implement a /settings command that allows players to toggle the visibility of their currency balances:
 Example command structure:
 plaintext
 ```/settings currency display ServerCoin/CosmeticCoin [on/off]```
 This command should interact with the player's profile settings to hide or show the currency display.
 ***Also about the currencies name is only temporally.*** 

# 2. HOW WILL BOTCOIN INTEGRATION OPERATE

Components Involved:

 **Minecraft Server:**
 **Server Type**: Use a server software like Spigot or Paper for better plugin support.
 
 **Plugins**: Utilize or create plugins like "Quests" for managing in-game tasks or quests.
 **Datorium Bot (Discord)**:
 _Existing bot that manages botcoin within Datorium Discord server._
 **Integration Mechanism:**
 
 **Step 1: Define Quests in Minecraft**
 Set up daily or periodic quests using the Minecraft server plugin. Examples could include:
 - Collecting a certain amount of wood.
 - Defeating a set number of mobs.
 - Completing a specific build challenge or puzzle.
 
 **Step 2: Track Quest Completion**
 When a player completes a quest, the Minecraft server plugin logs this completion, possibly through a custom command or an event listener in the plugin.
 
 **Step 3: Communication Between Minecraft and Discord**
 Automated Method: Develop a script or use a webhooks system:
 - Scripting: Write a script (e.g., in Python or JavaScript) that runs on the server or a separate machine, which:
 >- Connects to the Minecraft server to receive quest completion events.
 >- Communicates with the Datorium Bot API or webhook to update botcoin balances. 
 **variants:**
 1. *Webhooks: Set up a webhook in your Minecraft server that sends a message to a designated channel or directly to the Datorium Bot when a player completes a quest. The bot would then parse this message to update the user's botcoin balance.*
 2. *Set up a webhook in your Minecraft server that sends a message to a designated channel. Afterwards the team will look thru the quests to know if the reward is acquired in ethical/rule-abiding manners.*
 
 **Step 4: Botcoin Management on Discord**
 Once the Datorium Bot receives the information, it updates the user's botcoin balance accordingly. This could be done through:
 A command like **/addbotcoin @user** amount triggered by the script or webhook.
 An automated system within the bot that listens for specific messages or commands from the Minecraft server.
 __**Also the mutiplier system will effect the reward too**__



# 3. COMSETIC COIN INTEGRATION!!

## CosmeticCoin
Conversion: Players can convert Botcoin into CosmeticCoin at a predefined rate (e.g., 1 Botcoin = 10 CosmeticCoins) through the Datorium bot:
__This conversion should be managed externally via Discord to avoid any direct in-game transaction of Botcoin.__

## Usage: 
CosmeticCoin is used to purchase cosmetic items or ranks:

### Ranks:
- Custom Ranks: For 10 CosmeticCoins, players can create their own custom rank with unique colors and titles using a plugin like "LuckPerms". This allows personalization without affecting gameplay balance.

- Rank Boosts: Small boosts like a slight increase in chat priority or a unique chat color for 5 CosmeticCoins, ensuring they remain cosmetic and do not offer gameplay advantages.

- Temporary Rank Titles: For 3 CosmeticCoins, players can earn a temporary elite title for one week, visible in chat, enhancing their social profile on the server.

### Cosmetic Items:
- Custom Name Tags: For 2 CosmeticCoins, players can customize name tags for their items, giving them a personal touch without altering gameplay.

- Animated Signatures: With 7 CosmeticCoins, players can get animated text signatures that appear when they type in chat, adding flair to their communication.

- Special Fireworks: Players can buy unique fireworks displays for 5 CosmeticCoins, which can be used during events or personal celebrations, enhancing the visual experience without gameplay impact.

### Some different uses:
- Job Postings: For 2 CosmeticCoins and ServerCoins, players can post a custom job application, like offering 3 stacks of gold for 15,000 ServerCoins. This integrates the economy by allowing players to buy services or goods from each other in a regulated manner.

- Custom Particle Effects: For 8 CosmeticCoins, players could choose a unique particle effect when performing certain actions, like breaking blocks, enhancing visual flair without gameplay benefits.

- Dynamic Player Banners: Players can design their own banners that appear behind them in certain server areas for 5 CosmeticCoins, personalizing their presence on the server.

- Voting Influence: Spend 4 CosmeticCoins to gain extra votes in server-wide decisions or polls, giving players a say in non-critical server aspects like event themes or server mascots.

-  Special Music Discs: For 6 CosmeticCoins, players can unlock exclusive music discs that play unique server-made tunes, adding to the server's ambiance without affecting gameplay (Or even your own custom mades).


### Integration and Display:
Use plugins like "PlaceholderAPI" to show CosmeticCoin balances on scoreboards or in chat. 
Introduce a "/cosmetic" command where players can manage their CosmeticCoins, check available items, and customize their purchases:
>/cosmetic buy rank/title/item
>/cosmetic customize rank color
>/cosmetic check balance


# FEATURES IN SERVER

## 1. Block Claiming System
### Functionality: Players can claim blocks around their houses to prevent griefing. This system limits how many blocks one can claim individually to maintain balance and ensure that everyone has a fair chance to secure their space.
> -Implementation: Use a plugin like "GriefPrevention" or "WorldGuard" to allow players to claim land. Players can use a command like /claim to start the process, selecting an area with tools provided by the plugin.
> -Limitations: Each player might have a cap, e.g., 100 blocks, which can be expanded through gameplay achievements or by spending CosmeticCoin.

## 2. Guild System
### Functionality: Players can form guilds where guild members share claim blocks. If one player has 100 claim blocks and another has 100, together they can use these blocks to claim larger areas for their guild.
> Implementation: Implement using a plugin like "Factions" or "Clans" where:
> - Guild members can pool their claim blocks into a communal pool.
> - Use commands like /guild create, /guild join, /guild claim to manage guild activities.
> - Guild leaders or officers can decide how the claim blocks are used across guild properties.

3. Claim Expiration
Functionality: Claimed areas automatically expire if unused for one or two months. Players can extend their claim with CosmeticCoin.
Implementation: 
Plugin needs to track the last activity in a claimed area. 
Commands like /claim extend could be used to extend the claim period, costing CosmeticCoin. 
Notifications to players could remind them to extend or lose their claim.

## 4. Sitting Slabs
### Functionality: Slabs that allow players to sit within any block, but they exit where they entered to prevent glitching. If inside a block, the player begins to suffocate.
>Implementation: 
>Use or modify plugins like "Chairs" or "Sitting" to create this functionality. 
>These slabs could be bought with CosmeticCoins and placed like any other block. 
>When a player sits, their position is saved, ensuring they exit at the entry point.
>Cost could be set at, for instance, 3 CosmeticCoins per slab.

## 5. Automatic Starter Kits
### Functionality: Upon joining the server, players automatically receive a basic kit including stone tools and 20 bread to help them start.
> Implementation: 
> - Use a plugin like "EssentialsX" to set up automatic kit distribution. 
> - Configure the kit to include basic essentials like stone tools (pickaxe, axe, shovel, hoe, sword) and food (bread).
> - No keep inventory means players lose these items upon death, encouraging continuous engagement.

## 6. Server Jobs
### Functionality: Introduce job roles where players can earn ServerCoins by performing specific tasks associated with their job. The jobs include Lumberjack, Miner, and Ore Collector, each with its level progression system:
 - Lumberjack: 
> - Task: Chop down trees to gather wood. Higher levels might require or reward for specific types of wood or more complex forestry tasks.
> - Levels: Starts at level 1, where chopping a certain amount of wood gives 100 ServerCoins. As players level up, the amount of wood required and the reward increase, reaching up to 10k ServerCoins at level 60 for more extensive or challenging tasks.
- Miner: 
> - Task: Mine various blocks like stone, coal, iron, etc. Higher levels could involve deeper mining or mining specific rare ores.
> - Levels: Similar progression; starting with basic mining tasks for smaller rewards, escalating in difficulty and reward, with 10k ServerCoins possible at level 60 for significant mining achievements.
- Ore Collector: 
> - Task: Focus on collecting specific ores, possibly including rare ones like diamond or gold. Might include mining in specific biomes or areas.
> - Levels: Progress from collecting common ores for modest rewards to hunting and gathering rare ores for substantial rewards, with the cap at 10k ServerCoins for level 60.

## 7. Bot Programming Feature
### Functionality: This feature allows players to program bots to perform various non-combat tasks, enhancing gameplay with educational elements. The bots can be programmed for tasks like building or navigating, with different levels of complexity catering to both beginners and experienced coders.
### Implementation:
**Initial Version (Visual Programming):**
- Tool: A visual programming environment similar to Scratch or Blockly, integrated into Minecraft through a custom plugin or mod. This version is tailored for younger players or those new to coding.
>Tasks: 
>- Building Assistance: Bots can be programmed to create simple structures or patterns, helping players with basic construction tasks.
>- Traveling: Bots can follow predefined paths or move to designated coordinates, useful for exploration or setting up navigation >points.
**Advanced Version (Scripting Languages like Python or JavaScript):**
- Tool: An in-game or external coding environment where players can write scripts that interact with the Minecraft server via an API.
>Tasks:
>- Complex Building: Bots can interpret and execute more intricate building designs from blueprints or schematics.
>- Security Alerts: Program bots to monitor areas and notify players if an entity enters a specific radius (e.g., 10 blocks) through in->game messages or external notifications like Discord.
>- Resource Management: Bots can manage inventories, sort items, or support automated farming systems without directly harvesting >resources.

### Security and Fairness:
__Limitations: Bots are restricted from mining or directly gathering resources to ensure they don't become overpowered. Their purpose is to assist in automation or precision tasks.__

### Learning Progression:
- Tutorials: In-game guides or missions to teach coding basics, starting with visual programming and progressing to script writing.
- Example: A tutorial might guide players through programming a bot to build a basic structure, then advance to more complex tasks like dynamic responses to environmental changes.

**Levels of Complexity:**
> - Beginner: Focus on simple commands for movement and basic block placement.
> - Intermediate: Introduce concepts like loops and conditionals for more dynamic behavior.
> - Advanced: Allow for full scripting with event handling, integration with other server plugins, and complex logic.

# SERVER HOSTING

**THESE ALL ARE ROUGH ESTIMATES!!**

## Online hosting
### For 100 Players:
**Server Hosting:**
- RAM: With 8-12GB of RAM, which is suitable for 100 players, hosting plans can range widely:
- Monthly Cost: Approximately $20 to $50. 

**Examples:** 
- Shockbyte: Offers plans with 8GB+ RAM for around $20 to $30 per month.
- Apex Hosting: Similar specs might cost between $25 to $45 per month.

**Additional Features:** 
- DDoS Protection: Often included, but if not, could add $5-$10 per month.
- Automatic Backups: Might be additional or included, around $5-$10 if extra.

### __Total Monthly Cost: Around $25 to $65, depending on exact specifications, provider, and additional services.__

### For 250 Players:
**Server Hosting:**
- RAM: For 250 players, you might need at least 16-24GB of RAM to handle the load efficiently:
- Monthly Cost: This could range from $50 to $100.

**Examples:**
- MCProHosting: Plans with adequate RAM for this scale can start around $50 but might go up to $100 for premium features.
- BisectHosting: Similar capabilities might cost you between $60 to $90 per month.

**Additional Features:**
- DDoS Protection: Likely included at this tier, but if not, expect an additional $10-$20.
- Automatic Backups: Often included or an additional $10-$20 if not.

###  __Total Monthly Cost: Approximately $60 to $130, considering the RAM, CPU requirements, and any add-on services.__

## LOCAL SERVERS

**THESE ALL ARE ROUGH ESTIMATES!!**

### For 100 Players:
**Hardware:** 
- CPU: A mid-range processor like an Intel i5 or AMD Ryzen 5 would suffice, costing around $200 to $300.
- RAM: 8-12GB RAM, which could be part of a larger kit or an upgrade, approximately $50 to $100.
- Storage: An SSD for better performance, maybe around 250GB, would cost about $50.
**Total Hardware Cost: Approximately $300 - $450.**
- Monthly Electricity Cost: ~$60 to $85.
**Networking:** 
- Bandwidth: With 100 players, consider a good upload speed, potentially needing a dedicated or upgraded internet plan. Let's estimate an additional $20/month for bandwidth.
## Total Monthly Operating Cost: Around $80 to $105.

### For 250 Players:
**Hardware:**
- CPU: A more powerful server-grade CPU or multiple CPUs, like Intel Xeon or AMD EPYC, could cost $500 to $1000.
- RAM: 16-24GB, costing around $100 to $200.
- Storage: 500GB SSD, about $100.
**Total Hardware Cost: Roughly $700 - $1300.**
- Monthly Electricity Cost: ~$96 to $144.
**Networking:** 
- Bandwidth: Increased bandwidth requirements, adding another $30-$50 per month.
## Total Monthly Operating Cost: Around $126 to $194.

### For 500 Players:
**Hardware:**
- CPU: You might need to look into dual or quad CPU setups, costing $1000 to $2000.
- RAM: 32-64GB, around $200 to $400.
- Storage: 1TB SSD for multiple worlds or backups, around $150.
**Total Hardware Cost: Approximately $1350 - $2550.**
- Monthly Electricity Cost: ~$192 to $288.
**Networking:** 
- Bandwidth: Much higher bandwidth needs, potentially adding $50-$100 per month.
## Total Monthly Operating Cost: Approximately $242 to $388.

### For 1000 Players:
**Hardware:**
- CPU: High-end server CPUs or multiple servers, around $2000 to $4000.
- RAM: 64GB or more, $400 to $800.
- Storage: Multiple SSDs or even a RAID setup, $300 to $600.
**Total Hardware Cost: Roughly $2700 - $5400.**
- Monthly Electricity Cost: ~$240 to $480.
**Networking:** 
- Bandwidth: Consider a dedicated line or significant upgrade, adding $100-$200 per month.
## Total Monthly Operating Cost: Around $340 to $680.


