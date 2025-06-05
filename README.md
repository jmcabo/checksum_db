# checksum_db
This little script gets the hash or checksum of a whole directory and subdirs. You can update new files individually. You can check integrity of only a subdir, or update a single file. A json db is kept in the same directory.  You can also check if the dates and sizes of have changed without checking the contents. Based on 'hash_db'.

This is an explanation I gave to a friend on how to use it (in spanish, I'm from Argentina):

Para crear el checksum del directorio actual y todos sus subdirs:

          *checksum_db init*

Para que agrege los archivos recientemente copiados o agregados a un subdir:

          *checksum_db update*

Para listar los cambios de fecha o de archivos borrados y agregados (sin involucrar el checksumeado):

          *checksum_db status*

Para verificar:      checksum_db verify
soporta todos estos algoritmos:

blake2b, blake2s, md5, md5-sha1, sha1, sha224, sha256, sha384, sha3_224, sha3_256, sha3_384, sha3_512, sha512, sha512_224, sha512_256, sm3
Tiene mucha más funcionalidad que esa
Como el *dirsum*, que es un único checksum que representa todo el árbol de directorios, cambia un bit de cualquier archivo y ya da distinto.

Y el *dirsumnow*
Y buscar duplicados.
Y otro comando para generar el archivo SHA1SUM o MD5SUM, etc a partir del json db, que son lo usual standard.
Entonces para comparar dos mirror de un backup *no necesitás tener los dos conectados a la vez.*


--
