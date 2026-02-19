# MCP Google Map Server

A powerful Model Context Protocol (MCP) server providing comprehensive Google Maps API integration with streamable HTTP transport support and LLM processing capabilities.


## ✅ Testing Status

**This MCP server has been tested and verified to work correctly with:**

- Claude Desktop
- Dive Desktop
- MCP protocol implementations

All tools and features are confirmed functional through real-world testing.

## Features

### 🆕 Latest Updates

 - ℹ️  **Reminder: enable Places API (New) in https://console.cloud.google.com before using the new Place features.**


### 🗺️ Google Maps Integration

- **Location Search**

  - Search for places near a specific location with customizable radius and filters
  - Get detailed place information including ratings, opening hours, and contact details

- **Geocoding Services**

  - Convert addresses to coordinates (geocoding)
  - Convert coordinates to addresses (reverse geocoding)

- **Distance & Directions**

  - Calculate distances and travel times between multiple origins and destinations
  - Get detailed turn-by-turn directions between two points
  - Support for different travel modes (driving, walking, bicycling, transit)

- **Elevation Data**
  - Retrieve elevation data for specific locations

### 🚀 Advanced Features

- **Streamable HTTP Transport**: Latest MCP protocol with real-time streaming capabilities
- **Session Management**: Stateful sessions with UUID-based identification
- **Multiple Connection Support**: Handle multiple concurrent client connections
- **Echo Service**: Built-in testing tool for MCP server functionality


## Available Tools

The server provides the following tools:

### Google Maps Tools

1. **search_nearby** - Search for nearby places based on location, with optional filtering by keywords, distance, rating, and operating hours
2. **get_place_details** - Get detailed information about a specific place including contact details, reviews, ratings, and operating hours
3. **maps_geocode** - Convert addresses or place names to geographic coordinates (latitude and longitude)
4. **maps_reverse_geocode** - Convert geographic coordinates to a human-readable address
5. **maps_distance_matrix** - Calculate travel distances and durations between multiple origins and destinations
6. **maps_directions** - Get detailed turn-by-turn navigation directions between two locations
7. **maps_elevation** - Get elevation data (height above sea level) for specific geographic locations


### Project Structure

```
src/
├── cli.ts                    # Main CLI entry point
├── config.ts                 # Server configuration
├── index.ts                  # Package exports
├── core/
│   └── BaseMcpServer.ts     # Base MCP server with streamable HTTP
└── tools/
    └── maps/                # Google Maps tools
        ├── toolclass.ts     # Google Maps API client
        ├── searchPlaces.ts  # Maps service layer
        ├── searchNearby.ts  # Search nearby places
        ├── placeDetails.ts  # Place details
        ├── geocode.ts       # Geocoding
        ├── reverseGeocode.ts # Reverse geocoding
        ├── distanceMatrix.ts # Distance matrix
        ├── directions.ts    # Directions
        └── elevation.ts     # Elevation data
```

## Tech Stack

- **TypeScript** - Type-safe development
- **Node.js** - Runtime environment
- **Google Maps Services JS** - Google Maps API integration
- **Model Context Protocol SDK** - MCP protocol implementation
- **Express.js** - HTTP server framework
- **Zod** - Schema validation

## Security Considerations

- API keys are handled server-side for security
- DNS rebinding protection available for production
- Input validation using Zod schemas
- Error handling and logging
