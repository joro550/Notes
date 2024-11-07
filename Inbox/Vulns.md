

package: setuptools
[CVE-2024-6345](https://scout.docker.com/vulnerabilities/id/CVE-2024-6345?s=github&n=setuptools&t=pypi&vr=%3C70.0.0)

> A vulnerability in the `package_index` module of pypa/setuptools versions up to 69.1.1 allows for remote code execution via its download functions. These functions, which are used to download packages from URLs provided by users or retrieved from package index servers, are susceptible to code injection. If these functions are exposed to user-controlled inputs, such as package URLs, they can execute arbitrary commands on the system. The issue is fixed in version 70.0.

package : setuptools 
[CVE-2022-40897](https://scout.docker.com/vulnerabilities/id/CVE-2022-40897?s=github&n=setuptools&t=pypi&vr=%3C65.5.1)

>Python Packaging Authority (PyPA)'s setuptools is a library designed to facilitate packaging Python projects. Setuptools version 65.5.0 and earlier could allow remote attackers to cause a denial of service by fetching malicious HTML from a PyPI package or custom PackageIndex page due to a vulnerable Regular Expression in `package_index`. This has been patched in version 65.5.1.

package: werkzeug
[CVE-2024-34069](https://scout.docker.com/vulnerabilities/id/CVE-2024-34069?s=github&n=werkzeug&t=pypi&vr=%3C3.0.3)

>The debugger in affected versions of Werkzeug can allow an attacker to execute code on a developer's machine under some circumstances. This requires the attacker to get the developer to interact with a domain and subdomain they control, and enter the debugger PIN, but if they are successful it allows access to the debugger even if it is only running on localhost. This also requires the attacker to guess a URL in the developer's application that will trigger the debugger.

package: werkzeug
[CVE-2024-49767](https://scout.docker.com/vulnerabilities/id/CVE-2024-49767?s=github&n=werkzeug&t=pypi&vr=%3C%3D3.0.5)

> Applications using Werkzeug to parse `multipart/form-data` requests are vulnerable to resource exhaustion. A specially crafted form body can bypass the `Request.max_form_memory_size` setting.
> 
>The `Request.max_content_length` setting, as well as resource limits provided by deployment software and platforms, are also available to limit the resources used during a request. This vulnerability does not affect those settings. All three types of limits should be considered and set appropriately when deploying an application.

package: werkzeug 
[CVE-2023-46136](https://scout.docker.com/vulnerabilities/id/CVE-2023-46136?s=github&n=werkzeug&t=pypi&vr=%3C2.3.8)

> Werkzeug multipart data parser needs to find a boundary that may be between consecutive chunks. That's why parsing is based on looking for newline characters. Unfortunately, code looking for partial boundary in the buffer is written inefficiently, so if we upload a file that starts with CR or LF and then is followed by megabytes of data without these characters: all of these bytes are appended chunk by chunk into internal bytearray and lookup for boundary is performed on growing buffer.
> 
> This allows an attacker to cause a denial of service by sending crafted multipart data to an endpoint that will parse it. The amount of CPU time required can block worker processes from handling legitimate requests. The amount of RAM required can trigger an out of memory kill of the process. If many concurrent requests are sent continuously, this can exhaust or kill all available workers

package: werkzeug
[CVE-2024-49766](https://scout.docker.com/vulnerabilities/id/CVE-2024-49766?s=github&n=werkzeug&t=pypi&vr=%3C%3D3.0.5)
> On Python < 3.11 on Windows, `os.path.isabs()` does not catch UNC paths like `//server/share`. Werkzeug's `safe_join()` relies on this check, and so can produce a path that is not safe, potentially allowing unintended access to data. Applications using Python >= 3.11, or not using Windows, are not vulnerable.


package: python-jose
[CVE-2024-33663](https://scout.docker.com/vulnerabilities/id/CVE-2024-33663?s=github&n=python-jose&t=pypi&vr=%3C%3D3.3.0)

> python-jose through 3.3.0 has algorithm confusion with OpenSSH ECDSA keys and other key formats. This is similar to CVE-2022-29217.

package: python-jose 
[CVE-2024-33664](https://scout.docker.com/vulnerabilities/id/CVE-2024-33664?s=github&n=python-jose&t=pypi&vr=%3C%3D3.3.0)

> python-jose through 3.3.0 allows attackers to cause a denial of service (resource consumption) during a decode via a crafted JSON Web Encryption (JWE) token with a high compression ratio, aka a "JWT bomb." This is similar to CVE-2024-21319.

package: gunicorn 
[CVE-2024-1135](https://scout.docker.com/vulnerabilities/id/CVE-2024-1135?s=github&n=gunicorn&t=pypi&vr=%3C22.0.0)

> Gunicorn fails to properly validate Transfer-Encoding headers, leading to HTTP Request Smuggling (HRS) vulnerabilities. By crafting requests with conflicting Transfer-Encoding headers, attackers can bypass security restrictions and access restricted endpoints. This issue is due to Gunicorn's handling of Transfer-Encoding headers, where it incorrectly processes requests with multiple, conflicting Transfer-Encoding headers, treating them as chunked regardless of the final encoding specified. This vulnerability has been shown to allow access to endpoints restricted by gunicorn. This issue has been addressed in version 22.0.0.
> 
> To be affected users must have a network path which does not filter out invalid requests. These users are advised to block access to restricted endpoints via a firewall or other mechanism if they are unable to update.

package: ecdsa
[CVE-2024-23342](https://scout.docker.com/vulnerabilities/id/CVE-2024-23342?s=github&n=ecdsa&t=pypi&vr=%3C%3D0.18.0)

>python-ecdsa has been found to be subject to a Minerva timing attack on the P-256 curve. Using the `ecdsa.SigningKey.sign_digest()` API function and timing signatures an attacker can leak the internal nonce which may allow for private key discovery. Both ECDSA signatures, key generation, and ECDH operations are affected. ECDSA signature verification is unaffected. The python-ecdsa project considers side channel attacks out of scope for the project and there is no planned fix.

package: jinja
[CVE-2024-34064](https://scout.docker.com/vulnerabilities/id/CVE-2024-34064?s=github&n=jinja2&t=pypi&vr=%3C3.1.4)
>The `xmlattr` filter in affected versions of Jinja accepts keys containing non-attribute characters. XML/HTML attributes cannot contain spaces, `/`, `>`, or `=`, as each would then be interpreted as starting a separate attribute. If an application accepts keys (as opposed to only values) as user input, and renders these in pages that other users see as well, an attacker could use this to inject other attributes and perform XSS. The fix for the previous GHSA-h5c8-rqwp-cp95 CVE-2024-22195 only addressed spaces but not other characters.
>
>Accepting keys as user input is now explicitly considered an unintended use case of the `xmlattr` filter, and code that does so without otherwise validating the input should be flagged as insecure, regardless of Jinja version. Accepting _values_ as user input continues to be safe.

package: jinja 
[CVE-2024-22195](https://scout.docker.com/vulnerabilities/id/CVE-2024-22195?s=github&n=jinja2&t=pypi&vr=%3C3.1.3)

> The `xmlattr` filter in affected versions of Jinja accepts keys containing spaces. XML/HTML attributes cannot contain spaces, as each would then be interpreted as a separate attribute. If an application accepts keys (as opposed to only values) as user input, and renders these in pages that other users see as well, an attacker could use this to inject other attributes and perform XSS. Note that accepting keys as user input is not common or a particularly intended use case of the `xmlattr` filter, and an application doing so should already be verifying what keys are provided regardless of this fix.

package: zip 
[CVE-2024-5569](https://scout.docker.com/vulnerabilities/id/CVE-2024-5569?s=github&n=zipp&t=pypi&vr=%3C3.19.1)

> A Denial of Service (DoS) vulnerability exists in the jaraco/zipp library, affecting all versions prior to 3.19.1. The vulnerability is triggered when processing a specially crafted zip file that leads to an infinite loop. This issue also impacts the zipfile module of CPython, as features from the third-party zipp library are later merged into CPython, and the affected code is identical in both projects. The infinite loop can be initiated through the use of functions affecting the `Path` module in both zipp and zipfile, such as `joinpath`, the overloaded division operator, and `iterdir`. Although the infinite loop is not resource exhaustive, it prevents the application from responding. The vulnerability was addressed in version 3.19.1 of jaraco/zipp.

