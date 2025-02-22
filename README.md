# Telex Random Meal Suggestion

A Telex interval integration that suggests random meals on certain time interval.

## Features

- Suggests a random meal.

## Installation

```bash
git clone https://github.com/collab-rishi/hng12-stage3-telex_integration.git
cd hng12-stage3-telex_integration
npm install
```

## Usage

1. Start the application:

   ```bash
   node index.js
   ```

## Endpoints

### GET [/integration.json](http://_vscodecontentref_/2)

Returns the integration schema for the Telex interval integration.

**Response:**

```json
{
  "data": {
      "date": {
        "created_at": "2025-02-22",
        "updated_at": "2025-02-22"
      },
      "descriptions": {
        "app_name": "Daily Meal Suggestion",
        "app_description": "Suggests a random meal daily.",
        "app_logo": "https://dcassetcdn.com/design_img/375573/141837/141837_3031164_375573_image.jpg",
        "app_url": "https://deployed-app.com",
        "background_color": "#fff"
      },
      "is_active": true,
      "integration_category": "Communication & Collaboration",
      "integration_type": "interval",
      "key_features": [
        "Daily random meal suggestion"
      ],
      "author": "Kumar Rishi",
      "settings": [
        {
          "label": "interval",
          "type": "text",
          "required": true,
          "default": "*/3 * * * *"
        }
      ],
      "target_url": "",
      "tick_url": "https://deployed-app.com/tick",
    }
}
```

### POST /tick

**Request Body:**

```json
{
  "return_url": "https://ping.telex.im/v1/return/<your-test-telex-channel-id>",
  "settings": [
    {
      "label": "interval",
      "type": "text",
      "required": true,
      "default": "*/3 * * * *"
    }
  ]
}
```

**Response:**

```json
{
  "status": success,
}
```

## Contributing

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Make your changes.
4. Commit your changes (`git commit -m 'Add some feature'`).
5. Push to the branch (`git push origin feature-branch`).
6. Open a pull request.

## License

This project is licensed under the MIT License - see the LICENSE file for details.
