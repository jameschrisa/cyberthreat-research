# Comprehensive Guide to Using Recon-ng Modules

## 1. Installation
If you haven't installed Recon-ng yet:
```bash
git clone https://github.com/lanmaster53/recon-ng.git
cd recon-ng
pip install -r REQUIREMENTS
```

## 2. Starting Recon-ng
Launch Recon-ng by typing:
```bash
recon-ng
```

## 3. Basic Commands
- `help`: Display available commands
- `workspaces create <name>`: Create a new workspace
- `workspaces load <name>`: Load an existing workspace
- `modules search`: List all available modules
- `modules load <module_name>`: Load a specific module
- `info`: Display information about the loaded module
- `options set <option> <value>`: Set an option for the current module
- `run`: Execute the loaded module
- `back`: Return to the main menu
- `exit`: Exit Recon-ng

## 4. Working with Modules
1. Search for modules:
   ```
   [recon-ng] > modules search
   ```

2. Load a module:
   ```
   [recon-ng] > modules load recon/domains-hosts/bing_domain_web
   ```

3. View module info:
   ```
   [recon-ng][bing_domain_web] > info
   ```

4. Set module options:
   ```
   [recon-ng][bing_domain_web] > options set SOURCE example.com
   ```

5. Run the module:
   ```
   [recon-ng][bing_domain_web] > run
   ```

## 5. Managing Data
- `show hosts`: Display discovered hosts
- `show contacts`: Show gathered contact information
- `show credentials`: View any collected credentials
- `db insert hosts`: Manually add a host to the database

## 6. Advanced Usage
1. Chaining modules:
   ```
   [recon-ng] > modules load recon/domains-hosts/bing_domain_web
   [recon-ng][bing_domain_web] > options set SOURCE example.com
   [recon-ng][bing_domain_web] > run
   [recon-ng][bing_domain_web] > back
   [recon-ng] > modules load recon/hosts-hosts/resolve
   [recon-ng][resolve] > run
   ```

2. Using global options:
   ```
   [recon-ng] > options set TIMEOUT 60
   ```

3. Creating reports:
   ```
   [recon-ng] > modules load reporting/csv
   [recon-ng][csv] > options set FILENAME /path/to/report.csv
   [recon-ng][csv] > run
   ```

## 7. Best Practices
- Always use a separate workspace for each project
- Regularly update Recon-ng and its modules
- Be mindful of rate limiting when querying external services
- Review and verify the information gathered
- Comply with all applicable laws and regulations when using Recon-ng

Remember, Recon-ng is a powerful tool. Use it responsibly and ethically, and always obtain proper authorization before conducting reconnaissance activities.
