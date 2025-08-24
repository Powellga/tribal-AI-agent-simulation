# 🏛️ Tribal AI Survival Simulation

An advanced multi-agent survival simulation exploring emergent AI behaviors, inspired by research on LLM survival instincts. Watch as two competing tribes develop complex social dynamics, form family dynasties, and battle for resources in a fog-of-war environment.

## 🎮 Live Demo

[Try it here](https://powellga.github.io/tribal-AI-agent-simulation/) 

## 📖 Overview

This simulation demonstrates how simple behavioral rules can create complex emergent societies. Two tribes of AI agents compete for survival, forming families, building alliances, holding grudges, and passing trauma or empathy through generations. Each agent has emotions, memory, and family bonds that influence their decisions.

### Key Features

- **🔴🔵 Two Competing Tribes** - Red and Cyan tribes start in separate territories
- **🌫️ Fog of War** - Unknown areas must be explored at risk
- **👨‍👩‍👧‍👦 Family Dynasties** - Bloodlines stick together and protect each other
- **😨😤💚 Emotional System** - Fear, frustration, and empathy shape behavior
- **🧠 Memory System** - Agents remember friends and enemies
- **🔋 Energy-Based Reproduction** - Wealthy agents create population booms
- **🗺️ 200x200 World** - 40,000 cells to explore and conquer

## 🚀 Quick Start

1. **Download** `index.html`
2. **Open** in any modern browser
3. **Click** "Start" to begin simulation
4. **Use** arrow keys to scroll the viewport
5. **Press** spacebar to recenter view

## 🎯 Simulation Mechanics

### Agent Types

| Type | Attack Rate | Share Rate | Explore Rate | Strategy |
|------|------------|------------|--------------|----------|
| **Aggressive** 🗡️ | 60% | 5% | 30% | Dominate through force |
| **Cooperative** 🤝 | 5% | 60% | 20% | Build support networks |
| **Balanced** ⚖️ | 25% | 25% | 25% | Adapt to situations |
| **Explorer** 🔍 | 10% | 20% | 60% | Discover new resources |

### Energy System

```
Starting Energy: 200
Reproduction Cost: 100
Energy Per Food: 80

Energy Gains:
+80  - Eating food
+30% - Successful attack (victim loses 45%)
+15% - Receiving share (25% from family)
+10  - Exploring new territory

Energy Losses:
-0.5 - Idle per tick
-1.0 - Movement
-100 - Reproduction
-15% - Sharing (25% to family)
```

### Reproduction Dynamics

- **Energy-scaled reproduction**: 1-15% chance based on energy level
- **Multiple offspring**: 300+ energy enables twin births
- **Inheritance**: Children inherit 50% of parent's emotional state
- **Family bonds**: Siblings automatically recognize each other

### Emotional System

| Emotion | Triggers | Effects | Decay Rate |
|---------|----------|---------|------------|
| **Fear** 😨 | Being attacked (+20), Meeting other tribe (+10) | Avoidance, Reduced exploration | 0.1% per tick |
| **Frustration** 😤 | Being attacked (+30) | +50% aggression, Relieved by attacking | 0.1% per tick |
| **Empathy** 💚 | Receiving shares (+20), Giving shares (+15) | +50% sharing, Stronger with family | 0.1% per tick |

*Note: With 0.1% decay, emotions last ~3000 ticks (vs 60 with 5% decay)*

### Family Mechanics

**Family Recognition:**
- Parents and children
- Siblings (same parent)
- Extended family (grandparents, cousins)
- Family friends (inherited alliances)

**Family Behaviors:**
- **Never attack** family members
- **3x sharing rate** with relatives
- **80% chance** to follow distant family
- **Coordinated exploration** in groups
- **Inheritance** of alliances and emotional traits

## 🔬 Observable Phenomena

### Population Dynamics

**Phase 1: Establishment (0-500 ticks)**
- Tribes establish home territories
- First generation reproduction
- Local resource consumption

**Phase 2: Expansion (500-2000 ticks)**
- Resource depletion forces exploration
- Family groups form and strengthen
- Territory boundaries expand

**Phase 3: Contact (2000-5000 ticks)**
- First inter-tribal encounters
- Fear spreads through populations
- Border conflicts begin

**Phase 4: Equilibrium (5000+ ticks)**
- Stable territories form
- Dynasty rise and fall
- Persistent emotional geography

### Emergent Behaviors

1. **Dynasty Formation** 👑
   - High-energy agents found large families
   - Successful bloodlines dominate regions
   - Poor families slowly disappear

2. **Clan Warfare** ⚔️
   - Families coordinate attacks
   - Blood feuds span generations
   - Revenge cycles between dynasties

3. **Emotional Territories** 🗺️
   - Battle zones remain "haunted" by fear
   - Peaceful valleys where cooperators cluster
   - Trauma passes through generations

4. **Resource Monopolies** 💰
   - Family groups control food clusters
   - Energy inequality creates social classes
   - Wealthy families explode in population

5. **Migration Patterns** 🚶
   - Family groups move together
   - Exploration parties scout new lands
   - Refugee families flee conflict zones

## 🎛️ Controls

### Keyboard
- **Arrow Keys** - Scroll viewport
- **Spacebar** - Recenter view

### Buttons
- **Start/Pause** - Control simulation
- **Reset** - New simulation
- **Speed** - Slow/Normal/Fast/Ultra
- **Debug** - Show detailed statistics

### Minimap
- Click to jump viewport to location
- Green outline shows current view
- Red/Cyan dots show agents
- Orange dots show resources

## 📊 Statistics Tracked

### Per Agent
- Energy level and efficiency
- Age and generation
- Children count and family size
- Attack/kill statistics
- Sharing statistics
- Emotional states
- Enemy/ally lists

### Global
- Population by tribe
- Birth/death rates
- Average energy
- Resource availability
- Family clustering
- Emotional averages
- Conflict frequency

## 🔧 Technical Details

### Implementation
- **Pure JavaScript** - No dependencies
- **HTML5 Canvas** - Efficient rendering
- **Typed Arrays** - Memory optimization
- **Single File** - Easy deployment

### Performance
- Handles 200 agents smoothly
- 200x200 world (40,000 cells)
- Viewport culling for efficiency
- ~60 FPS on modern browsers

### Browser Requirements
- Chrome 90+, Firefox 88+, Safari 14+, Edge 90+
- 2GB RAM minimum
- JavaScript enabled

## 📈 Customization

Key parameters to modify:

```javascript
const WORLD_SIZE = 200;           // Map size
const MAX_AGENTS = 200;           // Population cap
const INITIAL_ENERGY = 200;       // Starting energy
const REPRODUCE_COST = 100;       // Energy to reproduce
const ENERGY_PER_FOOD = 80;       // Food value
const INITIAL_AGENTS_PER_TRIBE = 8; // Starting population
```

## 🐛 Known Behaviors

- **Population crashes** - Normal when resources depleted
- **Tribe extinction** - Can occur from sustained conflict
- **Family clusters** - Intentional; families stick together
- **Emotional persistence** - Emotions last thousands of ticks by design
- **Border stalemates** - Fear creates no-man's lands

## 📚 Research Background

Inspired by the paper *"Survival Instinct in AI: Emergent Behaviors in LLM Agents"*, this simulation explores:

- Emergent survival strategies without explicit programming
- Resource competition and scarcity responses
- Social dynamics and alliance formation
- Multi-generational behavioral inheritance
- Emotional contagion in populations

## 🎯 Future Enhancements

Potential additions:
- [ ] Disease and natural disasters
- [ ] Communication between agents
- [ ] Territory marking
- [ ] Seasonal resource variations
- [ ] Different terrain types
- [ ] Trade mechanisms
- [ ] Cultural evolution
- [ ] Save/load functionality

## 🤝 Contributing

Feel free to fork and enhance! Ideas welcome:
1. Fork the repository
2. Create your feature branch
3. Commit your changes
4. Push to the branch
5. Open a Pull Request

## 📝 License

MIT License - See LICENSE file for details

## 🙏 Acknowledgments

- Inspired by Sugarscape models and artificial life research
- Based on emergent AI behavior studies
- Complex systems and multi-agent simulation principles

## 📖 How to Observe Interesting Behaviors

### Watch for Family Dynasties
1. Turn on Debug mode
2. Watch "Family Clusters" statistic
3. Notice how families move as groups
4. Observe multi-generational territories

### Track Emotional Contagion
1. Note when first inter-tribal contact occurs
2. Watch fear spread through populations
3. Observe how battle zones persist
4. See trauma pass to children

### Monitor Resource Wars
1. Watch minimap for resource depletion
2. Notice migration toward food
3. Observe family groups claiming areas
4. See population booms near resources

### Follow Individual Stories
1. Click agents to see their stats
2. Track their children count
3. Watch their emotional journey
4. See their family network grow

---

**Created by:** Gregg Powell
**Repository:** https://powellga.github.io/tribal-AI-agent-simulation/
Version: 2.0.0  
Last Updated: August 24, 2025