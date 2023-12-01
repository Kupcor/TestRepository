#### [HIGH] Exploiting Interrupted Access - Modifying Cookie Parameters

**Description:**  
The application exhibits a vulnerability to interrupted access via Cookie file manipulation. This vulnerability allows access to the application with admin privileges.

**Necessary Conditions for Exploiting the Vulnerability:**
- Access to the application,
- A user account.

**Technical Details (Proof of Concept):**  
Admin functions access is stored in a cookie file. After logging in as a sample user `jack:jacktheripper`, the cookie's admin value is set to 0.
To confirm the existence of the vulnerability, the following steps should be performed:
1. Log in to the application as a user.
2. Open developer tools and locate the cookie file.  
   ![View of the cookie file in developer tools](img/A1_lab1_1.png)
3. Change the "admin" parameter value from 0 to 1.  
   ![Changing the cookie value - content displayed only for admins](img/A1_lab1_2.png)
4. The value accessible only to admins is now visible to a regular user - Secret Key.

**Notes:**  
None

**Location:** http://127.0.0.1:8000/broken_access_lab_1

**Recommendations:**
- Avoid storing sensitive information, such as user permissions, in cookies. Prefer storing session identifiers instead.
- Store session information on the server side, not the client side. This limits the risk of manipulating values stored in cookies.
- Encrypt information stored in cookies to hinder their interception and modification.
- Ensure that each operation requiring admin privileges is additionally checked on the server side.
- Set a short session duration, forcing regular user logins, thereby limiting the potential attack time.

**Further Information:**
- [OWASP Top 10 A01_2021-Broken Access Control](https://owasp.org/Top10/A01_2021-Broken_Access_Control/)
- [ECCouncil Cybersecurity Exchange - Broken Access Control Vulnerability](https://www.eccouncil.org/cybersecurity-exchange/web-application-hacking/broken-access-control-vulnerability/)
