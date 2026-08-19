## Part A — HTTP Capture

**What username and password were sent?**

Username: anna.virtanen
Password: Summer2026!

I found them in the HTTP POST data:
`username=anna.virtanen&password=Summer2026!&remember=on`

**Was the login submitted using GET or POST?**

The login was submitted using **POST**.

**What is the SESSIONID cookie, and why is it dangerous?**

The SESSIONID was:
`a3f9c2e7b81d4f60a5e2c9d10f4b7e88`

It was shown in the HTTP response as a `Set-Cookie` header.

This is dangerous because if an attacker steals the cookie they could potentially access the users logged-in session without knowing the password.

**What two sensitive pieces of information were visible on the dashboard?**

* Role: Finance Administrator
* Email: [anna.virtanen@pohjola-logistics.local](mailto:anna.virtanen@pohjola-logistics.local)

This information was visible because the website was using plain HTTP.

## Part B — HTTPS Capture

**Can the username and password be found in the HTTPS capture? Why or why not?**

No. The username and password are encrypted by TLS, so someone watching the network cannot easily read the login information.

**What is the server name shown in the Client Hello?**

The server name was `lab-portal.local`.

It was shown as the SNI in the TLS Client Hello.

**What can an eavesdropper still learn from the HTTPS capture?**

They can still see some information, such as IP addresses, packet sizes, and timing. However, they cannot see the actual encrypted website data.

## Part C — Making Sense of It

**Why does protocol choice matter for confidentiality?**

HTTP sends information in plain text, while HTTPS encrypts it. This means HTTPS is much safer for things like passwords and other private information.

**Give a daily-life example involving an untrusted network.**

For example, if I use public Wi-Fi at a coffee shop, HTTPS helps protect my web traffic from other people on the network. They may still be able to see some information like IP addresses and timing, but not the actual contents of the traffic.

**What surprised me**

What surprised me most was how easy it was to see the username, password, and session cookie in the HTTP capture. With HTTPS, the login information was hidden and only some basic network information was visible.
