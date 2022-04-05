[![Code style: black](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/psf/black)

# Simple-Script-To-Detect-Subdomain-Caching
A super simple Python script to detect if a file of subdomains contains caching. Works with IPs, domains, subdomains, etc.

# Usage
Like FFUF, but without the bruteforcing or FFUF part and web cache poisoning instead. URLs within text files must be in the format of "https://example.com". Command usage format is as follows:

-----------------------------------------------------------------
> python3 detcache domains
-----------------------------------------------------------------

OR

------------------------------------------------------------------
> python3 detcache domains cached-domains.txt
------------------------------------------------------------------

Both print the same results, but the second saves to a file named "cached-domains.txt"

# Options

### positional arguments:

  subdomain_file     the file of http (sub)domains
  
  outfile            the file to store output to

### optional arguments:
  
  -h, --help         show help message and exit
  
  -n, --no-sslcheck  ignore that a url does not have valid ssl
  
## Notes
