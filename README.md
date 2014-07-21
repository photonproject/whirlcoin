WhirlCoin Wallet

http://www.WhirlCoin.org

License

WhirlCoin is released under the terms of the MIT license. See `COPYING` for more
information or see http://opensource.org/licenses/MIT.


--- Howto build for Mac ---

Follow the preparation guide here: 
https://github.com/bitcoin/bitcoin/blob/master/doc/build-osx.md

Be carefull to the installation of berkelay-db4 (not berkelay-db) from brew repo, there is no need to update the formula, just brew update and track the one is fine. 
Ensure you are using the latest available version of boost libs, otherwise there is a known issue compiling on osx (brew upgrade boost in case you have it already installed)

Run qmake to adapt the makefile to your environment overwriting the existing one.
Modify Makefile to include:

`INCPATH, add -I/usr/local/opt/berkeley-db4/include`
`LIBPATH, add -L/usr/local/opt/berkeley-db4/lib`

