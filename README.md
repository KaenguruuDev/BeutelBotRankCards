# BeutelBotRankCards

A simple ASP.NET API for generating Discord rank cards.

## Features

- Custom rank card generation with user avatar, username, level, rank, and XP
- Configurable progress bar color
- PNG output format

## Requirements

- .NET 9.0

## Running

```bash
dotnet run
```

The API runs on `http://localhost:2052`.

## Endpoints

- `GET /` - API status page
- `POST /card/new` - Create a new rank card
- `GET /cards/{filename}` - Retrieve a generated card

## Card Request Format

```json
{
  "Username": "ExampleUser",
  "AvatarUrl": "https://cdn.discordapp.com/avatars/.../avatar.png",
  "GuildId": 123456789012345678,
  "UserId": 987654321098765432,
  "Xp": 1500,
  "Level": 5,
  "Rank": 3,
  "XpToNextLevel": 2000,
  "Progress": 75,
  "CardColor": "#5865F2"
}
```
