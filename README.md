# CronJobManager

CronJobManager is a project that helps manage and schedule cron jobs in a .NET Core application. It provides a robust and flexible framework for executing tasks at specified intervals.

## Table of Contents

- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Configuration](#configuration)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)

## Prerequisites

Before you begin, ensure you have the following installed:

- [.NET Core SDK](https://dotnet.microsoft.com/download)
- [SQL Server](https://www.microsoft.com/en-us/sql-server/sql-server-downloads)
- [Docker Desktop (optional, for containerization)](https://www.docker.com/products/docker-desktop)

Database CronJobaManager must exist in Sql Server before project is started
Project QueueAPI must be up and running before CronJobManager is started

## Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/gunnarsireus/CronJobManager.git
   cd CronJobManager

2. Restore the .NET Core packages:

    ````bash
    dotnet restore

3. Build the project:
    
    ````bash
    dotnet build

## Configuration

1. Update the connection strings in the `appsettings.json` file located in the root of the project.

2. Ensure the following configurations are correctly set:
   - **Database Connection Strings:** Point to your SQL Server instance.
   - **Cron Job Schedules:** Define the schedules for each cron job in the configuration.
   - **Environment Variables:** Set any required environment variables, such as logging settings or external service URLs.

3. Save the changes to the `appsettings.json` file.

## Usage

To run the application locally, execute the following command:
    
    ````bash
    dotnet run

The application will start managing the cron jobs based on the configurations provided in the appsettings.json.

For deployment, consider using Docker or integrating the service into a broader microservices architecture. For Docker, you may need to build the Docker image:

    ````bash
    docker build -t cronjobmanager .

And then run the container:

    ````bash
    docker run -d -p 8080:80 cronjobmanager


## Contributing

Contributions are welcome! If you'd like to contribute:

1. Fork the repository on GitHub.
2. Create a new branch from `main` for your feature or bugfix.
3. Make your changes, commit, and push to your branch.
4. Open a Pull Request against the `main` branch with a detailed description of your changes.

Please ensure that your code follows the project's coding standards and includes appropriate tests.

## License

This project is licensed under the MIT License. For more details, see the [LICENSE](LICENSE) file in the repository.
