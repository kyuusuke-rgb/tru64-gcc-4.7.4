GCC 4.7.4 for Tru64 UNIX (OSF/1 5.1b) - Binary Package
 Target: alphaev56-dec-osf5.1b
===================================================================

1. DESCRIPTION
   This package contains GCC 4.7.4 (C / C++) built natively via
   3-stage bootstrap on Tru64 UNIX v5.1b.
   It includes required libiconv.so.3.1.0 runtime binaries.

2. CONTENTS
   - /usr/local/gcc474
   - /usr/local/lib/libiconv.so*

3. EXTRACT / RESTORE
   Run the following commands as root to extract to /usr/local:

     cd /usr/local
     gzip -d -c /usr/local/src/Tru64_GCC_4.7.4_with_iconv.tar.gz | tar xvf -

4. ENVIRONMENT SETUP (.profile or .bashrc)
   Add the following lines to your user shell environment:

     export PATH=/usr/local/gcc474/bin:$PATH
     export LD_LIBRARY_PATH=/usr/local/gcc474/lib:/usr/local/lib:$LD_LIBRARY_PATH

5. ASSEMBLER (as) FIX
   If the compiler complains about missing 'as', link or copy
   the system assembler:

     mkdir -p /usr/local/gcc474/alphaev56-dec-osf5.1b/bin
     cp /usr/ccs/bin/as /usr/local/gcc474/alphaev56-dec-osf5.1b/bin/

6. VERIFICATION
   Test the installation using:

     gcc -v
     g++ -v

   Expected output: "gcc version 4.7.4 (GCC)"
===================================================================
