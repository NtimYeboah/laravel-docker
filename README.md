# laravel-docker
Minimal dockerized laravel environment

## Usage
Clone this repository to the base directory of your project
```bash
git clone https://github.com/NtimYeboah/laravel-docker.git
```

Change directory to the `laravel-docker/docker` directory and build the images
```bash
./build
```

Set the following environment variables similar to this in the `.env` file
`DB_HOST=mysql`
`REDIS_HOST=redis`

Modify the database environment variables in the `develop` file to the ones used with your application
```
export DB_ROOT_PASS=${DB_ROOT_PASS:-secret}
export DB_NAME=${DB_NAME:-homestead}
export DB_USER=${DB_USER:-root}
export DB_PASS=${DB_PASS:-secret}
```

Change directory to `laravel-docker` directory and start the containers in detached mode
```base
./develop up -d
```

## Running artisan command
To run artisan commands use `./develop artisan`.
Example to generate a controller file use `./develop artisan make:controller UsersController`