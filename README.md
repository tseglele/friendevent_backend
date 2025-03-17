# Friend Event Backend

This is the backend for the Friend Event application, built with Symfony.

## Prerequisites

Before you begin, ensure you have met the following requirements:
- You have installed PHP >= 8
- You have installed Composer
- You have installed Symfony CLI
- You have a running instance of a MySQL database

## Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/fredericBui/friendevent_backend.git
    ```

2. Navigate to the project directory:
    ```bash
    cd friendeventbackend
    ```

3. Install the dependencies:
    ```bash
    composer install
    ```

4. Set up the environment variables:
    ```bash
    cp .env .env.local
    ```
    Update the `.env.local` file with your database credentials.

5. Run the database migrations:
    ```bash
    php bin/console doctrine:migrations:migrate
    ```

## Usage

To start the development server, run:
```bash
symfony server:start
```

## All routes
```
/
/register
/login
/logout
/event
/event/new
/event/{id}
/event/{id}/edit
/event/{id}/register
/participation
/participation/new
/participation/{id}
/participation/{id}/edit
/participation/{id}/register
```

## How to use the API

After Register and create an event, go to /api
Perform a request from API plateform
Try this command on your terminal
```
curl -X 'GET' 'http://127.0.0.1:8000/api/events?page=1' -H 'accept: application/ld+json'
```

## Running Tests

To run the tests, execute:
```bash
php bin/phpunit
```

## Contributing

To contribute to this project, please fork the repository and create a pull request.

## License

This project is licensed under the MIT License.