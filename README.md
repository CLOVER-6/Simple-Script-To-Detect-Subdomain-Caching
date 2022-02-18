[![Code style: black](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/psf/black)

# Simple-Script-To-Detect-Subdomain-Caching
A super simple Python script to detect if a file of subdomains contains caching.

# Usage
Can be used much like masscan for web cache poisoning. URLs within text files must be in the format of "https://example.com". Command usage format is as follows:

-----------------------------------------------------------------
> cat domains.txt | python3 detcache cached-domains.txt
-----------------------------------------------------------------

OR

------------------------------------------------------------------
> echo "https://example.com" | python3 detcache cached-domains.txt
------------------------------------------------------------------
