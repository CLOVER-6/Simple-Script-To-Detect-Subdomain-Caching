[![Code style: black](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/psf/black)

# Simple-Script-To-Detect-Subdomain-Caching
A simple Python script to detect if a file of subdomains contains caching. Works with IPs, domains, subdomains, etc. This script is primarily for cache poisoning, cache DOSing, or cache information disclosure. See "Generalisation" for more info on this.

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

  -t TIMEOUT, --timeout TIMEOUT
                        set a timeout for url connection
  
# Generalisation
This script is primarily for cache poisoning, cache DOSing, or cache information disclosure, which is why the default behaviour detects cache-specific headers and cache-specific statuses (i.e. "HIT", "MISS", etc). If you want to make the script simply detect if the sites cached but not displaying status, follow the steps below:

- Open source code
- Go to Line 109 and Line 112 (this may have slight variance dependent on text editor and such, but photos are attached)
![image](https://github.com/CLOVER-6/Simple-Script-To-Detect-Subdomain-Caching/assets/89226564/ca538f16-2c39-4617-afbd-46c563811788)
- Remove Line 109 and the "and ifStatusPresent" in the if statement
![image](https://github.com/CLOVER-6/Simple-Script-To-Detect-Subdomain-Caching/assets/89226564/e4eab4fc-fd2f-4e85-a3f8-eeebca2f634c)
