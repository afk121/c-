Windows служба FileWatcher следит за папкой Directory:
1. FileCrypt.cs зашифровывает в UTF8 файл .txt формата, добавленный в указанную папку, благодаря методу класса FileCrypt.EncryptTo
2. После этого файл архивируется службой в папку Archived благодаря методу Archive этого же класса.
3. Затем файл расшифровывается в папку targetDirectory благодаря методу FileCrypt.DecryptTo.
4. Файл разархивируется в папку Crypted благодаря методу FileCrypt.UnArchive.
