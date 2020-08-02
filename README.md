# Python-SMTP
SMTPS (Simple Mail Transfer Protocol Secure) is a method for securing the SMTP using transport layer security. It is intended to provide authentication of the communication partners, as well as data integrity and confidentiality.

SMTPS is not a proprietary protocol and not an extension of SMTP. It is a way to secure SMTP at the transport layer, by wrapping SMTP inside TLS. Conceptually, it is similar to how HTTPS wraps HTTP inside TLS.

This means that the client and server speak normal SMTP at the application layer, but the connection is secured by SSL or TLS. This happens when the TCP connection is established, before any mail data has been exchanged. Since whether or not to use SSL or TLS is not explicitly negotiated by the peers, services that speak SMTPS are usually reachable on a dedicated port of their own.

User-level email clients typically use SMTP only for sending messages to a mail server for relaying, and typically submit outgoing email to the mail server on port 587 or 465 as per RFC 8314. For retrieving messages, IMAP and POP3 are standard, but proprietary servers also often implement proprietary protocols.


MIME
Multipurpose Internet Mail Extensions (MIME) is an Internet standard that extends the format of email messages to support text in character sets other than ASCII, as well as attachments of audio, video, images, and application programs. Message bodies may consist of multiple parts, and header information may be specified in non-ASCII character sets. Email messages with MIME formatting are typically transmitted with standard protocols, such as the Simple Mail Transfer Protocol (SMTP), the Post Office Protocol (POP), and the Internet Message Access Protocol (IMAP).

The MIME standard is specified in a series of requests for comments: RFC 2045, RFC 2046, RFC 2047, RFC 4288, RFC 4289 and RFC 2049. The integration with SMTP email is specified in RFC 1521 and RFC 1522.

Although the MIME formalism was designed mainly for SMTP, its content types are also important in other communication protocols. In the HyperText Transfer Protocol (HTTP) for the World Wide Web, servers insert a MIME header field at the beginning of any Web transmission. Clients use the content type or media type header to select an appropriate viewer application for the type of data indicated. Browsers typically contain GIF and JPEG image viewers.
