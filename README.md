# Umbraco Fundamentals

A modern Umbraco CMS project built with Umbraco 17.1.0, demonstrating fundamental concepts and best practices for building content-managed websites.

## Overview

This project showcases a complete Umbraco implementation featuring:

- **Umbraco CMS 17.1.0** - Latest version of the leading .NET CMS
- **Umbraco Forms 17.1.2** - For creating and managing forms
- **uSync 17.0.2** - Content synchronization and deployment
- **.NET 10.0** - Built on the latest .NET platform
- **Strongly-typed Models** - Generated content models for type-safe development

### Features

- Multiple content types including Blog, Shop, Products, and Text Pages
- Image management with custom crop aliases
- Form blocks for user interaction
- Rich text and media handling
- Organized Views with master templates
- Content synchronization with uSync

## Project Structure

- **UmbracoFundamentals.Models** - Contains generated content models and constants
- **UmbracoFundamentals.Website** - Main web application with views, configuration, and wwwroot

## Getting Started

### Prerequisites

- [.NET 10.0 SDK](https://dotnet.microsoft.com/download/dotnet/10.0) or later
- A code editor (Visual Studio 2022, VS Code, or Rider)
- SQL Server or SQL LocalDB for the database

### Initial setup

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd umbraco-fundamentals
   ```

2. **Restore dependencies**
   ```bash
   dotnet restore
   ```

3. **Configure local appsettings**
   - Copy `appsettings.json` to `appsettings.Local.json`
   - Update any settings in `appsettings.Local.json` as needed for your local environment

4. **Setup a local database**
   - Create a new empty SQL Server or SQL LocalDB database
   - Update the connection string in `appsettings.Local.json` to point to your local database

5. **Run the application**
   ```bash
   cd UmbracoFundamentals.Website
   dotnet run
   ```

6. **Access Umbraco**
   - Open your browser and navigate to `https://localhost:5001` (or the port shown in the terminal)
   - On first run, you'll be guided through the Umbraco installer
   - Create your admin account and select a database (LocalDB is recommended for development)

7. **Import content with uSync**
   - After installation, navigate to the Umbraco backoffice (`/umbraco`)
   - Go to the uSync section to import the included content and document types

### Development Configuration

The project uses local configuration overrides for development:
- Copy `appsettings.json` to `appsettings.Local.json` for local settings
- `appsettings.Local.json` is loaded in DEBUG mode and ignored by git

## License

See [LICENSE](LICENSE) file for details.