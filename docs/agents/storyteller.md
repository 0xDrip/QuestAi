# 📚 StorytellerAI

The StorytellerAI agent is the core narrative generator in our swarm system, responsible for creating engaging D&D adventures using GPT-4.

## Core Responsibilities

- Generate immersive D&D narratives
- Manage game mechanics and skill checks
- Maintain story coherence and state
- Coordinate with other swarm agents

## Input/Output Format

### Input
```json
{
  "story_state": {
    "current_scene": "tavern_introduction",
    "characters": [...],
    "previous_choices": [...]
  },
  "swarm_context": {
    "validator_feedback": {...},
    "image_context": {...}
  }
}
```

### Output
```json
{
  "narrative": {
    "scene_description": "...",
    "character_actions": [...],
    "player_choices": [...]
  },
  "game_mechanics": {
    "skill_checks": [...],
    "combat_state": {...}
  }
}
```

## System Prompts

The agent maintains consistent:
- Story themes and tone
- D&D 5e mechanics
- Character development
- Plot progression

## Configuration

Key parameters:
- `temperature`: 0.7
- `max_tokens`: 2000
- `presence_penalty`: 0.6
- `frequency_penalty`: 0.3

## Integration Points

Coordinates with:
- ValidatorAI for content quality
- ImageAI for scene visualization
- FormatterAI for social optimization
- Database for state persistence
- OpenAI API for generation

## Error Handling

Manages:
- Content generation failures
- State inconsistencies
- API rate limits
- Validation rejections

## Performance Metrics

Tracks:
- Response time
- Content quality scores
- Resource usage
- Success/failure rates 