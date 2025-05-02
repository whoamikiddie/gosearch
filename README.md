# GoSearch

GoSearch is a powerful username search tool written in Go that helps you find usernames across various websites and services. It also includes features to check for compromised credentials and domain availability.

## Features

- 🔍 Search usernames across multiple websites
- 🔒 Check for compromised credentials
- 🌐 Domain availability checking
- 🔐 Integration with HudsonRock's Cybercrime Intelligence Database
- 📊 Integration with BreachDirectory (requires API key)
- 🔑 Integration with ProxyNova for compromised password checking
- 📝 Automatic results saving to a text file

## Installation

```bash
# Clone the repository
git clone https://github.com/whoamikiddie/gosearch.git

# Navigate to the directory
cd gosearch

# Build the project
go build

# Run the program
./gosearch -u <username>
```

## Usage

Basic usage:
```bash
./gosearch -u <username>
```

With additional options:
```bash
# Disable false positives
./gosearch -u <username> --no-false-positives

# Search BreachDirectory with API key
./gosearch -u <username> -b <api_key>
# or
./gosearch -u <username> --breach-directory <api_key>
```

## Options

- `-u, --username`: Username to search (required)
- `--no-false-positives`: Do not show false positives
- `-b, --breach-directory`: Search BreachDirectory with an API key

## Output

The tool will:
1. Search for the username across multiple websites
2. Check HudsonRock's Cybercrime Intelligence Database
3. Search for compromised credentials on ProxyNova
4. Check domain availability
5. Save all results to a text file named `<username>.txt`

## API Keys

Some features require API keys:
- BreachDirectory: Get a free API key (10 lookups) at https://rapidapi.com/rohan-patra/api/breachdirectory

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## Issues

If you find any issues, please report them at: https://github.com/whoamikiddie/gosearch/issues

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- Thanks to all the services that make this tool possible
- Special thanks to the open-source community for their contributions 