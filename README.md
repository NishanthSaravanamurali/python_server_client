# python_server_client

In this I have tried two different ideas of uploading files to a server and downlooading files from a server


first idea: there is no integrity checking of the file by the client and the file can be tampered in server

second idea: client builds merkel tree and stores the the root node in a binary file, which it uses to check the integrity of the file while receiving back from server else deletes it. IE only those files which are uploaded by the client can be downloaded back and for others to access it, they need the binary file containing the root node.

third idea: (Even though this idea is not implemmented it similar to second one) client builds the merkel node and sends a copy to server to check whether the file was not tampered while transit. while downloading the merkel node is again sent back so the client can check the integrity of the file being downloaded. this removes the constraint that only those who uploaded a specific file can download it back
