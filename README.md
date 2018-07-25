# Cookie-Injection-Attack
The same origin policy of cookies separates the content of one domain from another. However, this works in unusual way in the case of cookies. The isolation of domain of cookies is weak. The secure flag of cookies ensure that the cookie should be sent over HTTPS connection only however the cookie can be set with the value of secure flag true from HTTP connection also. Hence cookies can be sent over HTTPS connection that are set by HTTP connection.For example, a cautious user might only visit news websites at open wireless networks. But an attacker can inject malicious cookies to poison her browser, and compromise her bank account when she later logs on to her bank site at home.
There is an unusual behaviour of cookies. Cookies are set and stored as a name/domain/path to value attributes mapping, but only name-value pairs are presented to both Javascript and web servers. This asymmetry allows cookies with the same name but different domain and/or path scopes to be written into browser; a subsequent reader can read out all same name cookies together, yet cannot distinguish them because the other attributes such as path are not presented in the reading process. Also, an origin for a given URL is defined by a 3-tuple: scheme, e.g. HTTP or HTTPS, domain and port. However, the security policy of cookies does not provide separation based on either scheme or port but only on domain.In addition, a website can set cookies with flexible domain scopes: 1) not shared (i.e., host-only), 2) shared with its subdomains, or 3) shared with its sibling domains.
Because of these reasons,the integrity of the cookie from an active Man In The Middle (MITM) or a malicious related domain that shares some cookie domain scope with it cannot be preserved.

# Types of Cookie Injections
## Cookie Overwriting: 
If a cookie shares the domain scope with a related domain, it can be directly overwritten by that domain using another cookie with the exactly same name/domain/path.
## Cookie Shadowing: 
An attacker with the control of a related domain can in- tentionally shadow a cookie by injecting another one that has the same name, but different domain/path scope.

# Steps
Created two web server using Xampp server. Both Server have same suffix domain. One is attacker website and other is valid server.Now user visited valid website, this website set a cookie. User visited attacker website and this website over write cookie set by the valid server.




