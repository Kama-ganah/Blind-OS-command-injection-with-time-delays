# Overview
I evaluated the input handling and command execution logic of a web application’s feedback feature. During testing, I identified a blind OS command injection vulnerability caused by unsafe inclusion of user-controlled input in shell commands. Although command output was not reflected in HTTP responses, successful exploitation was confirmed using a time-based technique that introduced a deliberate delay in server responses. This project demonstrates how blind command injection flaws can be reliably identified and exploited even in the absence of direct output.

# Methodology

Step 1: Intercepted and analyzed feedback submission requests to identify command execution points.

Step 2: Injected a time-delay payload into the email parameter to trigger OS-level command execution.

Step 3: Measured server response times to detect execution of the injected command.

Step 4: Verified the vulnerability by observing consistent, controlled response delays.

# Conclusion

This assessment confirmed a critical blind OS command injection vulnerability that allows arbitrary command execution on the server. The findings highlight the risks of improper input sanitization and the effectiveness of time-based techniques for detecting blind command injection flaws.
