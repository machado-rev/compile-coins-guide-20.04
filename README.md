## STEP 1: Go to the root folder of the coin and do the command

> sudo ./contrib/install_db4.sh `pwd`

## STEP 2: Do the export command
> export BDB_PREFIX='/root_of_coin/db4'

## STEP 3: Use the configure 
> ./configure BDB_LIBS="-L${BDB_PREFIX}/lib -ldb_cxx-4.8" BDB_CFLAGS="-I${BDB_PREFIX}/include"

## STEP 4: If you are compiling the daemon use
> ./configure BDB_LIBS="-L${BDB_PREFIX}/lib -ldb_cxx-4.8" BDB_CFLAGS="-I${BDB_PREFIX}/include" --without-gui --enable-bitcore-rpc

## STEP 4: do the normal compilation
> make -j2
