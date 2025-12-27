DBD_API

A specialized .NET Core backend designed to interface with Steam and Dead by Daylight (DbD) data. This API handles Steam depot downloads, processes game files (PAK files) using UE4 tools, and serves data to a Vue.js frontend.
🚀 Features

    Steam Integration: Automated login and depot management using SteamKit2.

    PAK File Processing: Utilizes UETools to read and extract Unreal Engine assets.

    Hybrid Caching: Supports both in-memory caching and Redis for distributed environments.

    SPA Hosting: Integrated hosting for a Vue.js frontend via SpaServices.

    Static Data Serving: Specialized endpoint for serving processed game assets with HTTPS compression.

🛠 Tech Stack

    Framework: .NET Core 3.0

    Languages: C#, TypeScript (Frontend)

    Caching: Redis / IDistributedCache

    Dependencies: * SteamKit2 (Steam communication)

        UETools (Unreal Engine asset parsing)

        RestSharp (API requests)

        Vue.js (Frontend framework)

📋 Prerequisites

Before running the application, ensure you have the following installed:

    .NET Core 3.0 SDK

    Node.js (for building the SPA)

    A valid Steam account (to fetch game data)

⚙️ Configuration

The application requires specific configuration keys in your appsettings.json or environment variables:
Key	Description
steam_user	Your Steam account username
steam_pass	Your Steam account password
redis:config	(Optional) Redis connection string
redis:instance	(Optional) Redis instance name

    Note: On the first run, the application will automatically create a data directory at ./data/381210 to store downloaded assets.
