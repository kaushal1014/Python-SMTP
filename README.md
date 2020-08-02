# Python-SMTP
SMTPS (Simple Mail Transfer Protocol Secure) is a method for securing the SMTP using transport layer security. It is intended to provide authentication of the communication partners, as well as data integrity and confidentiality.

SMTPS is not a proprietary protocol and not an extension of SMTP. It is a way to secure SMTP at the transport layer, by wrapping SMTP inside TLS. Conceptually, it is similar to how HTTPS wraps HTTP inside TLS.

This means that the client and server speak normal SMTP at the application layer, but the connection is secured by SSL or TLS. This happens when the TCP connection is established, before any mail data has been exchanged. Since whether or not to use SSL or TLS is not explicitly negotiated by the peers, services that speak SMTPS are usually reachable on a dedicated port of their own.

User-level email clients typically use SMTP only for sending messages to a mail server for relaying, and typically submit outgoing email to the mail server on port 587 or 465 as per RFC 8314. For retrieving messages, IMAP and POP3 are standard, but proprietary servers also often implement proprietary protocols.
