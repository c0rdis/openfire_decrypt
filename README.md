# openfire_decrypt
Little java tool to decrypt passwords from Openfire embedded-db.
<br>
Originally published at https://hashcat.net/forum/archive/index.php?thread-2399.html


<h4>Compilation:</h4>
<code> javac OpenFireDecryptPass.java </code>

<h4>Launch & output:</h4>
<code> java OpenFireDecryptPass 08f62fb6091259a2be869ae0ace90f600ec3729a9d5d4683 UaNTQtUV6S7kwm9 </code>

<code> hashcat (hex: 0068006100730068006300610074) </code>

<h4> Known issue:</h4>
Failure to decrypt due to lack of unlimited strength files. Example of error:

<code> Exception in thread "main" java.security.InvalidKeyException: Illegal key size </code>

<code> ... at OpenFireDecryptPass.main(OpenFireDecryptPass.java:26) </code>

<h4> Solution:</h4>
Download the necessary files and install them in <code>${java.home}/jre/lib/security/</code>

URLs to download:

<a href="http://www.oracle.com/technetwork/java/javase/downloads/jce-6-download-429243.html">Java Cryptography Extension (JCE) Unlimited Strength Jurisdiction Policy Files 6</a>

<a href="http://www.oracle.com/technetwork/java/javase/downloads/jce-7-download-432124.html">Java Cryptography Extension (JCE) Unlimited Strength Jurisdiction Policy Files 7</a>

<a href="http://www.oracle.com/technetwork/java/javase/downloads/jce8-download-2133166.html">Java Cryptography Extension (JCE) Unlimited Strength Jurisdiction Policy Files 8</a>
