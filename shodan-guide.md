# Shodan: Common Research Strings and Practical Tips for Beginners

## Introduction
Shodan is a search engine for Internet-connected devices. This guide provides common search strings and practical tips for novice cyberthreat researchers.

## Common Research Strings

1. Find servers with default credentials:
   ```
   "default password"
   ```

2. Discover webcams:
   ```
   webcam has_screenshot:true
   ```

3. Find open databases:
   ```
   "MongoDB Server Information" port:27017
   ```

4. Locate devices with open SSH:
   ```
   "SSH-2.0-OpenSSH" port:22
   ```

5. Find FTP servers with anonymous login:
   ```
   "220" "FTP server ready" port:21
   ```

6. Discover IoT devices:
   ```
   "Server: yawcam" "Mime-Type: text/html"
   ```

7. Find servers vulnerable to Heartbleed:
   ```
   vuln:CVE-2014-0160
   ```

8. Locate devices with default/simple passwords:
   ```
   "Authentication: Disabled" port:8080
   ```

9. Find printers:
   ```
   "HTTP/1.1 200 OK" "Server: EPSON_Linux" port:80
   ```

10. Discover industrial control systems:
    ```
    "Schneider Electric" port:502
    ```

## Practical Tips

1. Use filters to narrow results:
   - `country:` (e.g., `country:US`)
   - `port:` (e.g., `port:80`)
   - `os:` (e.g., `os:Linux`)

2. Combine search terms:
   ```
   apache country:DE city:"Berlin"
   ```

3. Use quotation marks for exact phrases:
   ```
   "default password"
   ```

4. Exclude results with minus sign:
   ```
   apache -country:US
   ```

5. Use logical operators:
   ```
   webcam AND has_screenshot:true
   ```

6. Leverage Shodan Dorks:
   - `hostname:` to search for specific hostnames
   - `net:` to search within IP ranges

7. Always respect ethical boundaries and legal restrictions.

8. Use Shodan's API for more advanced searches and automation.

9. Regularly update your knowledge of new Shodan features and search capabilities.

10. Practice responsible disclosure if you discover vulnerabilities.

Remember, as a beginner, focus on understanding the results and their implications rather than attempting to exploit any vulnerabilities you might discover.
