

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