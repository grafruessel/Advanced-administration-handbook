# Security

The goal of the page is to inform users who manage a WordPress site about general security best practices both in terms of environment level items, such as file permissions, as well as application-level items, such as setting up proper user roles, so they have a better foundation for security than setting up WordPress somewhere with no additional configuration.

The most important thing to do for WordPress security is to keep WordPress itself and all installed plugins and themes up to date. It is also encouraged for users to choose themes and plugins that are actively receiving updates.

WordPress is committed to providing a secure experience for users. Information about WordPress’s official stance on security and a general discussion about WordPress’s overall aims for security can be found on WordPress.org’s Security page.

This guide borrows heavily from the WordPress Codex’s guide on Hardening WordPress. Since it’s publicly editable, advice in the codex should be viewed with caution.

Keeping any system, not just WordPress, secure is continuous work. Good security requires careful planning, monitoring, and periodic maintenance.

Security largely consists of reducing risk and planning for recovery. Most security plans focus on minimizing the risk of unauthorized access only, but risk can never be successfully reduced to zero. As long as there is some risk, you must plan for recovery so that if something were to happen, user sites are not completely lost and can be quickly restored to normal operation.

Security is also about more than WordPress. It is also about making sure your hosting environment is secure and your personal online practices and behaviors keep you safe. Good security depends on the technology in use and the people using the technology. Obsolete or out-of-date technology can have bugs or vulnerabilities that can put your WordPress website at risk. People’s bad online practices can also put your WordPress website as risk. It is important to make sure that not only do you keep the technology you use up-to-date and maintained but also that employees are using security best practices when using the Internet and when interacting with your hosting platform or customer WordPress sites.

## Throttling multiple login attempts

One of the most common kinds of attacks targeting internet services is brute force login attacks. With this form of attack, a malicious party tries to guess WordPress usernames and passwords. The attacker needs only the URL of a user site to perform an attack. Software is readily available to perform these attacks using botnets, making increasingly complex passwords easier to find.

The best protection against this kind of attack is to set and recommend and/or enforce strong passwords for WordPress users.

It is also recommended for hosts to throttle login attempts at the network and server level when possible. It’s helpful to throttle both maximum logins per site over time, and maximum attempts per IP over time across server or infrastructure to mitigate bot password brute-force attacks. This can be done at the plugin level as well, but not without incurring the additional resource utilization caused during these attacks.

## A Note About Usernames

Some WordPress security guides recommend using unique usernames for WordPress administrator accounts. While well-intentioned, WordPress’s REST API allows anyone to view many of the users for your WordPress website. You can see this for yourself by sending a request to the endpoint at /wp-json/wp/v2/users.

<!info>The WordPress project doesn’t consider usernames or user IDs to be private or secure information. A username is part of your online identity. It is meant to identify, not verify, who you are saying you are. Verification is the job of the password.</info>

## Two-Factor Authentication

Two-factor authentication, also known as 2FA or two-step authentication, is a login scheme that uses a separate, second form of authentication when a user attempts to log in to a service with two-factor authentication enabled. The exact two-factor authentication setup varies from service to service, but it usually involves entering a code or interacting with an application on a smartphone when attempting to log in to a service. WordPress does not have two-factor authentication by default; however, [there are several plugins that provide two-factor authentication for self-hosted WordPress websites](https://wordpress.org/plugins/tags/two-factor-authentication).

## Changelog

- 2022-08-16: Nothing here, yet.
