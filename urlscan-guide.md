# urlscan.io: Common Research Strings and Practical Tips for Beginners

## Introduction
urlscan.io is a free service to scan and analyze websites. This guide provides common search queries and practical tips for novice cyberthreat researchers.

## Common Research Strings

1. Find potentially malicious PDFs:
   ```
   filename:.pdf AND tag:malicious
   ```

2. Discover phishing sites impersonating a brand:
   ```
   domain:paypal.com -task.url:paypal.com
   ```

3. Locate sites using specific vulnerable software:
   ```
   server:Apache/2.4.49
   ```

4. Find sites loading content from specific IPs:
   ```
   ip:123.456.789.0
   ```

5. Discover sites with specific SSL certificates:
   ```
   cert.subject.cn:"*.cloudfront.net"
   ```

6. Locate WordPress sites:
   ```
   body:"/wp-content/"
   ```

7. Find sites using specific JavaScript libraries:
   ```
   filename:jquery.min.js
   ```

8. Discover potentially compromised sites:
   ```
   page.status:200 AND hash:eacb
   ```

9. Locate sites with open directories:
   ```
   "Index of /" AND mimetype:text/html
   ```

10. Find sites with specific HTTP headers:
    ```
    header.x-powered-by:PHP/7.2
    ```

## Practical Tips

1. Use the Advanced Search feature for complex queries.

2. Combine multiple search terms:
   ```
   domain:example.com AND filename:admin.php
   ```

3. Use quotation marks for exact phrases:
   ```
   "login page"
   ```

4. Exclude results with minus sign:
   ```
   wordpress -domain:wordpress.com
   ```

5. Leverage urlscan.io's tagging system:
   ```
   tag:phishing AND tag:scam
   ```

6. Use date ranges to focus on recent scans:
   ```
   date:>2023-01-01
   ```

7. Analyze the visual site content using the screenshot feature.

8. Examine the "Indicators" tab for potential security issues.

9. Use the "HTTP" tab to analyze all requests made by the scanned site.

10. Check the "Console" tab for JavaScript errors that might indicate malicious behavior.

11. Always verify findings and avoid jumping to conclusions based on a single scan.

12. Use the urlscan.io API for automation and integration with other tools.

13. Regularly check urlscan.io's blog and Twitter for updates on new features and best practices.

Remember, as a beginner, focus on understanding the results and their context. Always respect privacy and legal boundaries when conducting research.
