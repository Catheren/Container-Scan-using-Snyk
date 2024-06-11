# Container-Scan-using-Snyk


C:\Users\jcath\Downloads\Snyk>docker --verion
^C
C:\Users\jcath\Downloads\Snyk>
C:\Users\jcath\Downloads\Snyk>docker --version
Docker version 26.1.1, build 4cf5afa

C:\Users\jcath\Downloads\Snyk>docker pull python:3.4-alpine
3.4-alpine: Pulling from library/python
8e402f1a9c57: Pull complete
cda9ba2397ef: Pull complete
aafecf9bbbfd: Pull complete
bc2e7e266629: Pull complete
e1977129b756: Pull complete
Digest: sha256:c210b660e2ea553a7afa23b41a6ed112f85dbce25cbcb567c75dfe05342a4c4b
Status: Downloaded newer image for python:3.4-alpine
docker.io/library/python:3.4-alpine

What's Next?
  1. Sign in to your Docker account → docker login
  2. View a summary of image vulnerabilities and recommendations → docker scout quickview python:3.4-alpine

C:\Users\jcath\Downloads\Snyk>snyk-win.exe container test python:3.4-alpine
`snyk` requires an authenticated account. Please run `snyk auth` and try again.

C:\Users\jcath\Downloads\Snyk>snyk auth
'snyk' is not recognized as an internal or external command,
operable program or batch file.

C:\Users\jcath\Downloads\Snyk>snyk-win.exe auth

Now redirecting you to our auth page, go ahead and log in,
and once the auth is complete, return to this prompt and you'll
be ready to start using snyk.

If you can't wait use this url:
https://app.snyk.io/login?token=7056eff4-1706-4c82-984d-dc25f29bb4df&utm_medium=cli&utm_source=cli&utm_campaign=CLI_V1_PLUGIN&utm_campaign_content=1.1291.1&os=windows_nt&docker=false


Your account has been authenticated. Snyk is now ready to be used.


C:\Users\jcath\Downloads\Snyk>snyk-win.exe container test python:3.4-alpine

Testing python:3.4-alpine...

✗ Low severity vulnerability found in openssl/libcrypto1.1
  Description: Inadequate Encryption Strength
  Info: https://security.snyk.io/vuln/SNYK-ALPINE39-OPENSSL-1089236
  Introduced through: openssl/libcrypto1.1@1.1.1a-r1, openssl/libssl1.1@1.1.1a-r1, apk-tools/apk-tools@2.10.3-r1, libtls-standalone/libtls-standalone@2.7.4-r6, ca-certificates/ca-certificates@20190108-r0
  From: openssl/libcrypto1.1@1.1.1a-r1
  From: openssl/libssl1.1@1.1.1a-r1 > openssl/libcrypto1.1@1.1.1a-r1
  From: apk-tools/apk-tools@2.10.3-r1 > openssl/libcrypto1.1@1.1.1a-r1
  and 5 more...
  Image layer: Introduced by your base image (python:3.4.10-alpine3.9)
  Fixed in: 1.1.1j-r0

✗ Low severity vulnerability found in openssl/libcrypto1.1
  Description: Use of a Broken or Risky Cryptographic Algorithm
  Info: https://security.snyk.io/vuln/SNYK-ALPINE39-OPENSSL-505098
  Introduced through: openssl/libcrypto1.1@1.1.1a-r1, openssl/libssl1.1@1.1.1a-r1, apk-tools/apk-tools@2.10.3-r1, libtls-standalone/libtls-standalone@2.7.4-r6, ca-certificates/ca-certificates@20190108-r0
  From: openssl/libcrypto1.1@1.1.1a-r1
  From: openssl/libssl1.1@1.1.1a-r1 > openssl/libcrypto1.1@1.1.1a-r1
  From: apk-tools/apk-tools@2.10.3-r1 > openssl/libcrypto1.1@1.1.1a-r1
  and 5 more...
  Image layer: Introduced by your base image (python:3.4.10-alpine3.9)
  Fixed in: 1.1.1d-r0

✗ Medium severity vulnerability found in sqlite/sqlite-libs
  Description: Divide By Zero
  Info: https://security.snyk.io/vuln/SNYK-ALPINE39-SQLITE-487067
  Introduced through: sqlite/sqlite-libs@3.26.0-r3, .python-rundeps@0
  From: sqlite/sqlite-libs@3.26.0-r3
  From: .python-rundeps@0 > sqlite/sqlite-libs@3.26.0-r3
  Image layer: '' | tr ',' '\n' | sort -u | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' | xargs -rt apk add --no-cache --virtual .python-rundeps'
  Fixed in: 3.28.0-r1

✗ Medium severity vulnerability found in sqlite/sqlite-libs
  Description: NULL Pointer Dereference
  Info: https://security.snyk.io/vuln/SNYK-ALPINE39-SQLITE-587452
  Introduced through: sqlite/sqlite-libs@3.26.0-r3, .python-rundeps@0
  From: sqlite/sqlite-libs@3.26.0-r3
  From: .python-rundeps@0 > sqlite/sqlite-libs@3.26.0-r3
  Image layer: '' | tr ',' '\n' | sort -u | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' | xargs -rt apk add --no-cache --virtual .python-rundeps'
  Fixed in: 3.28.0-r2

✗ Medium severity vulnerability found in openssl/libcrypto1.1
  Description: NULL Pointer Dereference
  Info: https://security.snyk.io/vuln/SNYK-ALPINE39-OPENSSL-1089231
  Introduced through: openssl/libcrypto1.1@1.1.1a-r1, openssl/libssl1.1@1.1.1a-r1, apk-tools/apk-tools@2.10.3-r1, libtls-standalone/libtls-standalone@2.7.4-r6, ca-certificates/ca-certificates@20190108-r0
  From: openssl/libcrypto1.1@1.1.1a-r1
  From: openssl/libssl1.1@1.1.1a-r1 > openssl/libcrypto1.1@1.1.1a-r1
  From: apk-tools/apk-tools@2.10.3-r1 > openssl/libcrypto1.1@1.1.1a-r1
  and 5 more...
  Image layer: Introduced by your base image (python:3.4.10-alpine3.9)
  Fixed in: 1.1.1k-r0

✗ Medium severity vulnerability found in openssl/libcrypto1.1
  Description: NULL Pointer Dereference
  Info: https://security.snyk.io/vuln/SNYK-ALPINE39-OPENSSL-1089233
  Introduced through: openssl/libcrypto1.1@1.1.1a-r1, openssl/libssl1.1@1.1.1a-r1, apk-tools/apk-tools@2.10.3-r1, libtls-standalone/libtls-standalone@2.7.4-r6, ca-certificates/ca-certificates@20190108-r0
  From: openssl/libcrypto1.1@1.1.1a-r1
  From: openssl/libssl1.1@1.1.1a-r1 > openssl/libcrypto1.1@1.1.1a-r1
  From: apk-tools/apk-tools@2.10.3-r1 > openssl/libcrypto1.1@1.1.1a-r1
  and 5 more...
  Image layer: Introduced by your base image (python:3.4.10-alpine3.9)
  Fixed in: 1.1.1i-r0

✗ Medium severity vulnerability found in openssl/libcrypto1.1
  Description: Integer Overflow or Wraparound
  Info: https://security.snyk.io/vuln/SNYK-ALPINE39-OPENSSL-1089234
  Introduced through: openssl/libcrypto1.1@1.1.1a-r1, openssl/libssl1.1@1.1.1a-r1, apk-tools/apk-tools@2.10.3-r1, libtls-standalone/libtls-standalone@2.7.4-r6, ca-certificates/ca-certificates@20190108-r0
  From: openssl/libcrypto1.1@1.1.1a-r1
  From: openssl/libssl1.1@1.1.1a-r1 > openssl/libcrypto1.1@1.1.1a-r1
  From: apk-tools/apk-tools@2.10.3-r1 > openssl/libcrypto1.1@1.1.1a-r1
  and 5 more...
  Image layer: Introduced by your base image (python:3.4.10-alpine3.9)
  Fixed in: 1.1.1j-r0

✗ Medium severity vulnerability found in openssl/libcrypto1.1
  Description: CVE-2019-1547
  Info: https://security.snyk.io/vuln/SNYK-ALPINE39-OPENSSL-491992
  Introduced through: openssl/libcrypto1.1@1.1.1a-r1, openssl/libssl1.1@1.1.1a-r1, apk-tools/apk-tools@2.10.3-r1, libtls-standalone/libtls-standalone@2.7.4-r6, ca-certificates/ca-certificates@20190108-r0
  From: openssl/libcrypto1.1@1.1.1a-r1
  From: openssl/libssl1.1@1.1.1a-r1 > openssl/libcrypto1.1@1.1.1a-r1
  From: apk-tools/apk-tools@2.10.3-r1 > openssl/libcrypto1.1@1.1.1a-r1
  and 5 more...
  Image layer: Introduced by your base image (python:3.4.10-alpine3.9)
  Fixed in: 1.1.1d-r0

✗ Medium severity vulnerability found in openssl/libcrypto1.1
  Description: Use of Insufficiently Random Values
  Info: https://security.snyk.io/vuln/SNYK-ALPINE39-OPENSSL-501158
  Introduced through: openssl/libcrypto1.1@1.1.1a-r1, openssl/libssl1.1@1.1.1a-r1, apk-tools/apk-tools@2.10.3-r1, libtls-standalone/libtls-standalone@2.7.4-r6, ca-certificates/ca-certificates@20190108-r0
  From: openssl/libcrypto1.1@1.1.1a-r1
  From: openssl/libssl1.1@1.1.1a-r1 > openssl/libcrypto1.1@1.1.1a-r1
  From: apk-tools/apk-tools@2.10.3-r1 > openssl/libcrypto1.1@1.1.1a-r1
  and 5 more...
  Image layer: Introduced by your base image (python:3.4.10-alpine3.9)
  Fixed in: 1.1.1d-r0

✗ Medium severity vulnerability found in openssl/libcrypto1.1
  Description: Information Exposure
  Info: https://security.snyk.io/vuln/SNYK-ALPINE39-OPENSSL-588019
  Introduced through: openssl/libcrypto1.1@1.1.1a-r1, openssl/libssl1.1@1.1.1a-r1, apk-tools/apk-tools@2.10.3-r1, libtls-standalone/libtls-standalone@2.7.4-r6, ca-certificates/ca-certificates@20190108-r0
  From: openssl/libcrypto1.1@1.1.1a-r1
  From: openssl/libssl1.1@1.1.1a-r1 > openssl/libcrypto1.1@1.1.1a-r1
  From: apk-tools/apk-tools@2.10.3-r1 > openssl/libcrypto1.1@1.1.1a-r1
  and 5 more...
  Image layer: Introduced by your base image (python:3.4.10-alpine3.9)
  Fixed in: 1.1.1d-r2

✗ Medium severity vulnerability found in musl/musl
  Description: Out-of-bounds Write
  Info: https://security.snyk.io/vuln/SNYK-ALPINE39-MUSL-1042761
  Introduced through: musl/musl@1.1.20-r4, bzip2/libbz2@1.0.6-r6, expat/expat@2.2.6-r0, gdbm/gdbm@1.13-r1, libffi/libffi@3.2.1-r6, libressl/libressl2.7-libssl@2.7.5-r0, ncurses/ncurses-libs@6.1_p20190105-r0, readline/readline@7.0.003-r1, sqlite/sqlite-libs@3.26.0-r3, xz/xz-libs@5.2.4-r0, zlib/zlib@1.2.11-r1, .python-rundeps@0, busybox/busybox@1.29.3-r10, alpine-baselayout/alpine-baselayout@3.1.0-r3, openssl/libcrypto1.1@1.1.1a-r1, openssl/libssl1.1@1.1.1a-r1, apk-tools/apk-tools@2.10.3-r1, libtls-standalone/libtls-standalone@2.7.4-r6, busybox/ssl_client@1.29.3-r10, ca-certificates/ca-certificates@20190108-r0, pax-utils/scanelf@1.2.3-r0, libc-dev/libc-utils@0.7.1-r0, musl/musl-utils@1.1.20-r4
  From: musl/musl@1.1.20-r4
  From: bzip2/libbz2@1.0.6-r6 > musl/musl@1.1.20-r4
  From: expat/expat@2.2.6-r0 > musl/musl@1.1.20-r4
  and 22 more...
  Image layer: '' | tr ',' '\n' | sort -u | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' | xargs -rt apk add --no-cache --virtual .python-rundeps'
  Fixed in: 1.1.20-r6

✗ High severity vulnerability found in sqlite/sqlite-libs
  Description: CVE-2019-19244
  Info: https://security.snyk.io/vuln/SNYK-ALPINE39-SQLITE-1019958
  Introduced through: sqlite/sqlite-libs@3.26.0-r3, .python-rundeps@0
  From: sqlite/sqlite-libs@3.26.0-r3
  From: .python-rundeps@0 > sqlite/sqlite-libs@3.26.0-r3
  Image layer: '' | tr ',' '\n' | sort -u | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' | xargs -rt apk add --no-cache --virtual .python-rundeps'
  Fixed in: 3.28.0-r2

✗ High severity vulnerability found in sqlite/sqlite-libs
  Description: Use After Free
  Info: https://security.snyk.io/vuln/SNYK-ALPINE39-SQLITE-449762
  Introduced through: sqlite/sqlite-libs@3.26.0-r3, .python-rundeps@0
  From: sqlite/sqlite-libs@3.26.0-r3
  From: .python-rundeps@0 > sqlite/sqlite-libs@3.26.0-r3
  Image layer: '' | tr ',' '\n' | sort -u | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' | xargs -rt apk add --no-cache --virtual .python-rundeps'
  Fixed in: 3.28.0-r0

✗ High severity vulnerability found in sqlite/sqlite-libs
  Description: Improper Initialization
  Info: https://security.snyk.io/vuln/SNYK-ALPINE39-SQLITE-587441
  Introduced through: sqlite/sqlite-libs@3.26.0-r3, .python-rundeps@0
  From: sqlite/sqlite-libs@3.26.0-r3
  From: .python-rundeps@0 > sqlite/sqlite-libs@3.26.0-r3
  Image layer: '' | tr ',' '\n' | sort -u | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' | xargs -rt apk add --no-cache --virtual .python-rundeps'
  Fixed in: 3.28.0-r3

✗ High severity vulnerability found in openssl/libcrypto1.1
  Description: Improper Certificate Validation
  Info: https://security.snyk.io/vuln/SNYK-ALPINE39-OPENSSL-1089232
  Introduced through: openssl/libcrypto1.1@1.1.1a-r1, openssl/libssl1.1@1.1.1a-r1, apk-tools/apk-tools@2.10.3-r1, libtls-standalone/libtls-standalone@2.7.4-r6, ca-certificates/ca-certificates@20190108-r0
  From: openssl/libcrypto1.1@1.1.1a-r1
  From: openssl/libssl1.1@1.1.1a-r1 > openssl/libcrypto1.1@1.1.1a-r1
  From: apk-tools/apk-tools@2.10.3-r1 > openssl/libcrypto1.1@1.1.1a-r1
  and 5 more...
  Image layer: Introduced by your base image (python:3.4.10-alpine3.9)
  Fixed in: 1.1.1k-r0

✗ High severity vulnerability found in openssl/libcrypto1.1
  Description: Integer Overflow or Wraparound
  Info: https://security.snyk.io/vuln/SNYK-ALPINE39-OPENSSL-1089235
  Introduced through: openssl/libcrypto1.1@1.1.1a-r1, openssl/libssl1.1@1.1.1a-r1, apk-tools/apk-tools@2.10.3-r1, libtls-standalone/libtls-standalone@2.7.4-r6, ca-certificates/ca-certificates@20190108-r0
  From: openssl/libcrypto1.1@1.1.1a-r1
  From: openssl/libssl1.1@1.1.1a-r1 > openssl/libcrypto1.1@1.1.1a-r1
  From: apk-tools/apk-tools@2.10.3-r1 > openssl/libcrypto1.1@1.1.1a-r1
  and 5 more...
  Image layer: Introduced by your base image (python:3.4.10-alpine3.9)
  Fixed in: 1.1.1j-r0

✗ High severity vulnerability found in openssl/libcrypto1.1
  Description: Use of a Broken or Risky Cryptographic Algorithm
  Info: https://security.snyk.io/vuln/SNYK-ALPINE39-OPENSSL-340660
  Introduced through: openssl/libcrypto1.1@1.1.1a-r1, openssl/libssl1.1@1.1.1a-r1, apk-tools/apk-tools@2.10.3-r1, libtls-standalone/libtls-standalone@2.7.4-r6, ca-certificates/ca-certificates@20190108-r0
  From: openssl/libcrypto1.1@1.1.1a-r1
  From: openssl/libssl1.1@1.1.1a-r1 > openssl/libcrypto1.1@1.1.1a-r1
  From: apk-tools/apk-tools@2.10.3-r1 > openssl/libcrypto1.1@1.1.1a-r1
  and 5 more...
  Image layer: Introduced by your base image (python:3.4.10-alpine3.9)
  Fixed in: 1.1.1b-r1

✗ High severity vulnerability found in openssl/libcrypto1.1
  Description: NULL Pointer Dereference
  Info: https://security.snyk.io/vuln/SNYK-ALPINE39-OPENSSL-588029
  Introduced through: openssl/libcrypto1.1@1.1.1a-r1, openssl/libssl1.1@1.1.1a-r1, apk-tools/apk-tools@2.10.3-r1, libtls-standalone/libtls-standalone@2.7.4-r6, ca-certificates/ca-certificates@20190108-r0
  From: openssl/libcrypto1.1@1.1.1a-r1
  From: openssl/libssl1.1@1.1.1a-r1 > openssl/libcrypto1.1@1.1.1a-r1
  From: apk-tools/apk-tools@2.10.3-r1 > openssl/libcrypto1.1@1.1.1a-r1
  and 5 more...
  Image layer: Introduced by your base image (python:3.4.10-alpine3.9)
  Fixed in: 1.1.1g-r0

✗ High severity vulnerability found in expat/expat
  Description: XML External Entity (XXE) Injection
  Info: https://security.snyk.io/vuln/SNYK-ALPINE39-EXPAT-453353
  Introduced through: expat/expat@2.2.6-r0, .python-rundeps@0
  From: expat/expat@2.2.6-r0
  From: .python-rundeps@0 > expat/expat@2.2.6-r0
  Image layer: '' | tr ',' '\n' | sort -u | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' | xargs -rt apk add --no-cache --virtual .python-rundeps'
  Fixed in: 2.2.7-r0

✗ High severity vulnerability found in expat/expat
  Description: Out-of-bounds Read
  Info: https://security.snyk.io/vuln/SNYK-ALPINE39-EXPAT-485094
  Introduced through: expat/expat@2.2.6-r0, .python-rundeps@0
  From: expat/expat@2.2.6-r0
  From: .python-rundeps@0 > expat/expat@2.2.6-r0
  Image layer: '' | tr ',' '\n' | sort -u | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' | xargs -rt apk add --no-cache --virtual .python-rundeps'
  Fixed in: 2.2.7-r1

✗ Critical severity vulnerability found in sqlite/sqlite-libs
  Description: Out-of-bounds Read
  Info: https://security.snyk.io/vuln/SNYK-ALPINE39-SQLITE-449671
  Introduced through: sqlite/sqlite-libs@3.26.0-r3, .python-rundeps@0
  From: sqlite/sqlite-libs@3.26.0-r3
  From: .python-rundeps@0 > sqlite/sqlite-libs@3.26.0-r3
  Image layer: '' | tr ',' '\n' | sort -u | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' | xargs -rt apk add --no-cache --virtual .python-rundeps'
  Fixed in: 3.28.0-r0

✗ Critical severity vulnerability found in musl/musl
  Description: Out-of-bounds Write
  Info: https://security.snyk.io/vuln/SNYK-ALPINE39-MUSL-458529
  Introduced through: musl/musl@1.1.20-r4, bzip2/libbz2@1.0.6-r6, expat/expat@2.2.6-r0, gdbm/gdbm@1.13-r1, libffi/libffi@3.2.1-r6, libressl/libressl2.7-libssl@2.7.5-r0, ncurses/ncurses-libs@6.1_p20190105-r0, readline/readline@7.0.003-r1, sqlite/sqlite-libs@3.26.0-r3, xz/xz-libs@5.2.4-r0, zlib/zlib@1.2.11-r1, .python-rundeps@0, busybox/busybox@1.29.3-r10, alpine-baselayout/alpine-baselayout@3.1.0-r3, openssl/libcrypto1.1@1.1.1a-r1, openssl/libssl1.1@1.1.1a-r1, apk-tools/apk-tools@2.10.3-r1, libtls-standalone/libtls-standalone@2.7.4-r6, busybox/ssl_client@1.29.3-r10, ca-certificates/ca-certificates@20190108-r0, pax-utils/scanelf@1.2.3-r0, libc-dev/libc-utils@0.7.1-r0, musl/musl-utils@1.1.20-r4
  From: musl/musl@1.1.20-r4
  From: bzip2/libbz2@1.0.6-r6 > musl/musl@1.1.20-r4
  From: expat/expat@2.2.6-r0 > musl/musl@1.1.20-r4
  and 22 more...
  Image layer: '' | tr ',' '\n' | sort -u | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' | xargs -rt apk add --no-cache --virtual .python-rundeps'
  Fixed in: 1.1.20-r5

✗ Critical severity vulnerability found in bzip2/libbz2
  Description: Out-of-bounds Write
  Info: https://security.snyk.io/vuln/SNYK-ALPINE39-BZIP2-452847
  Introduced through: bzip2/libbz2@1.0.6-r6, .python-rundeps@0
  From: bzip2/libbz2@1.0.6-r6
  From: .python-rundeps@0 > bzip2/libbz2@1.0.6-r6
  Image layer: '' | tr ',' '\n' | sort -u | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' | xargs -rt apk add --no-cache --virtual .python-rundeps'
  Fixed in: 1.0.6-r7



Organization:      catheren
Package manager:   apk
Project name:      docker-image|python
Docker image:      python:3.4-alpine
Platform:          linux/amd64
Base image:        python:3.4.10-alpine3.9
Licenses:          enabled

Tested 28 dependencies for known issues, found 23 issues.

Base Image               Vulnerabilities  Severity
python:3.4.10-alpine3.9  23               3 critical, 9 high, 9 medium, 2 low

Recommendations for base image upgrade:

Alternative image types
Base Image                     Vulnerabilities  Severity
python:3.13.0b1-slim           50               1 critical, 1 high, 0 medium, 48 low
python:3.9.19-slim-bookworm    54               1 critical, 1 high, 0 medium, 52 low
python:3.13.0b1-slim-bullseye  77               1 critical, 1 high, 0 medium, 75 low
python:3.13.0b1-bookworm       205              2 critical, 2 high, 0 medium, 201 low

Alpine 3.9.2 is no longer supported by the Alpine maintainers. Vulnerability detection may be affected by a lack of security updates.

Learn more: https://docs.snyk.io/products/snyk-container/getting-around-the-snyk-container-ui/base-image-detection
