# Generate and encrypt passwords

Generates true random passwords using /dev/urandom, with the emphasis on security over pronounceability. It can also encrypt plaintext passwords given in a temporary file.

Package info: https://packages.debian.org/jessie/makepasswd

## Manual

```
makepasswd(1)                UNIX Reference Manual               makepasswd(1)



NAME
       makepasswd - generate and/or encrypt passwords

SYNOPSIS
       makepasswd [ --chars N ] [ --clearfrom file ] [ --count N ] [ --crypt |
       --nocrypt | --crypt-md5 ] [ --cryptsalt N ] [ --help ] [ --maxchars N ]
       [ --minchars N ] [ --randomseed N ] [ --rerandom N ] [ --repeatpass N ]
       [ --string string ] [ --verbose | --noverbose ]

DESCRIPTION
       makepasswd generates true random passwords using /dev/urandom, with the
       emphasis on security over pronounceability.  It can also encrypt plain-
       text passwords given on the command line.

OPTIONS
       --chars N
              Generate passwords with exactly N characters (do  not  use  with
              options --minchars and --maxchars).

       --clearfrom FILE
              Use   password   from  FILE  instead  of  generating  passwords.
              Requires the --crypt or the --crypt-md5 options; may not be used
              with  these  options:  --chars, --maxchars, --minchars, --count,
              --string, --nocrypt.  Trailing newlines are  removed  but  other
              white space is not.

       --count N
              Produce a total of N passwords (the default is one).

       --crypt
              Produce encrypted passwords.

       --crypt-md5
              Produce  encrypted  passwords  using the MD5 digest (hash) algo-
              rithm.

       --cryptsalt N
              Use crypt() salt N, a positive number <= 4096.  If random  seeds
              are desired, specify a zero value (the default).

       --help Ignore other operands and produce only a help display.

       --maxchars N
              Generate passwords with at most N characters (default = 10).

       --minchars N
              Generate passwords with at least N characters (default = 8).

       --nocrypt
              Do not encrypt the generated password(s) (the default).

       --noverbose
              Display no labels on output (the default).

       --randomseed N
              Use  random number seed N, between 0 and 2^32 inclusive.  A zero
              value results in a real-random seed.  This generates  much  less
              secure  passwords  than  the  default; not only does it generate
              predictable passwords due to the fixed seed, but  the  range  of
              available  seeds is 32 bits rather than the default of 256 bits,
              and cannot be changed without breaking expectations of  previous
              users of this option.  If possible, do not use this option.

       --rerandom N
              Set  the random seed value every N values used.  Specify zero to
              use a single seed value (the default). Specify one to get  true-
              random  passwords,  though  note  that doing this too frequently
              will deplete the supply of entropy  available  in  the  kernel's
              entropy pool.

       --repeatpass N
              Use each password N times (4096 maximum, --crypt must be set and
              --cryptsalt may not be set).

       --string STRING
              Use the characters in STRING to generate random passwords.

       --verbose
              Display labelling information on output.

HISTORY
       makepasswd was originally part of the mkircconf program  used  to  cen-
       trally  administer  the Linux Internet Support Cooperative IRC network.
       It may potentially be of use in any situation where passwords  must  be
       secure and need not be memorized by humans.

       Colin  Watson modified it to use OpenSSL's pseudo-random number genera-
       tor.

COPYRIGHT
       Copyright (c) 1997-1998 by lilo <lilo@linpeople.org>.  All  rights  are
       reserved  by  the  author.  This program may be used under the terms of
       version 2 of the GNU Public License.

SEE ALSO
       passwd(5)



Debian Distribution             1998 February 9                  makepasswd(1)
```

Source: https://manpages.debian.org/cgi-bin/man.cgi?query=makepasswd&apropos=0&sektion=0&manpath=Debian+8+jessie&format=html&locale=en
