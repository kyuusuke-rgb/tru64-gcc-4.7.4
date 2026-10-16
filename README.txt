===================================================================
 GCC 4.7.4 for Tru64 UNIX (OSF/1 5.1b) - Binary Package
 Target: alphaev56-dec-osf5.1b
===================================================================

1. DESCRIPTION
   This package contains GCC 4.7.4 (C / C++) built natively via
   3-stage bootstrap on Tru64 UNIX v5.1b.
   It includes required libiconv.so.3.1.0 runtime binaries.

2. EXTRACT & FIX SYMLINKS
   Run the following commands as root to extract and fix broken links:

     # cd /usr/local
     # gzip -dc /path/to/Tru64_GCC_4.7.4_with_iconv.tar.gz | /sbin/tar xvf -

     # Fix libiconv symlinks in /usr/local/lib
     # cd /usr/local/lib
     # ln -sf libiconv.so.3.1.0 libiconv.so
     # ln -sf libiconv.so.3.1.0 libiconv.so.2
     # ln -sf libiconv.so.3.1.0 libiconv.so.3

3. ENVIRONMENT SETUP (.profile)
   Add the following lines to your user shell environment:

     export PATH=/usr/local/gcc474/bin:$PATH
     export LD_LIBRARY_PATH=/usr/local/lib:$LD_LIBRARY_PATH

4. VERIFICATION
   Test the installation using:

     # gcc -v
     # /usr/local/bin/tar --version
===================================================================
