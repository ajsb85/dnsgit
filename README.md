#A DnsGit Demo for DnsGit

```
    ____     _   __   _____    ______   ____   ______
   / __ \   / | / /  / ___/   / ____/  /  _/  /_  __/
  / / / /  /  |/ /   \__ \   / / __    / /     / /   
 / /_/ /  / /|  /   ___/ /  / /_/ /  _/ /     / /    
/_____/  /_/ |_/   /____/   \____/  /___/    /_/       
```

#What is DnsGit
[DnsGit](https://dnsgit.com) is an awesome DNS manange service.

    Git(Manage) ➩ DnsGit(middle ware)  ➩ DNSPod(resolve)


#Concept & Syntax

## Domain-File
file named by domain name.

##Record-Line 
one record mapping one line in domain file.

Syntax:

```
-- @type[required]  = record type(A, CNAME, MX, NS ...)
-- @name[required]  = relative name
-- @value[required] = record value(ipadress, domain ...)
-- @ttl[optional]   = TTL (default: user default TTL)
-- @mx[optional]    = MX Priority (default: 5)

type(name, value, ttl, mx)

```
Example:
```
A(@, 1.1.1.1, 默认, 600)
CNAME(dnsgit, dnsgit.com, 默认, 600)
MX(@, mxdomain.qq.com., 默认, 600, 10)

```

