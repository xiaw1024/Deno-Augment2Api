# Deno-Augment2Api

A Deno-based API proxy service for Augment that provides a web interface for managing authentication tokens.

## Features

- Web-based token management interface
- Secure API key authentication
- Token generation and management
- Real-time token status updates
- Responsive design with modern UI
- Support for multiple tenants

## Prerequisites

- [Deno](https://deno.land/) (version 1.x or higher)
- An Augment account and API access

## Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/Deno-Augment2Api.git
cd Deno-Augment2Api
```

2. Create a `.env` file in the root directory with your API key:
```env
API_KEY=your_api_key_here
```

## Usage

1. Start the server:
```bash
deno run --allow-net --allow-env --allow-read main.ts
```

2. Open your browser and navigate to:
```
http://localhost:4242
```

3. Enter your API key in the web interface

4. Use the interface to:
   - View current tokens
   - Generate new tokens
   - Delete existing tokens
   - Refresh token list

## API Endpoints

- `GET /auth` - Get authorization URL
- `POST /getToken` - Submit authorization response to get token
- `GET /getTokens` - Get list of current tokens
- `DELETE /deleteToken/:token` - Delete a specific token
- `POST /v1/chat/completions` - Chat completion endpoint

## Security

- All API endpoints require authentication via API key
- Tokens are stored securely using Deno KV
- API keys are never stored in the frontend
- All sensitive operations require API key validation

## Development

The project structure:
```
.
├── main.ts           # Main server implementation
├── static/          # Static files
│   └── index.html   # Web interface
├── types.ts         # TypeScript type definitions
└── .env            # Environment variables
```

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Author

- [lpp](https://github.com/xiaojia21190)

## Acknowledgments

- Built with [Deno](https://deno.land/)
- Web framework: [Oak](https://deno.land/x/oak)
- UI components: [Bootstrap Icons](https://icons.getbootstrap.com/)
