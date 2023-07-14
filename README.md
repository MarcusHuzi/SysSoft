# SysSoft

Para decriptar o programa, criamos uma biblioteca dinâmica que sobrescreve a função de autorização utilizada no programa docrypt.

Para compilar a bilbioteca, execute o comando makefile:

    ```bash
    make -f Makefile2
    ```

Isso irá gerar o arquivo libhackfile.so.

Por fim, para executar o programa utilizando esta biblioteca execute:

    ```bash
    make -f Makefile2 run
    ```

O programa pedirá por credenciais de usuário e senha, basta digitar qualquer coisa.

Em seguida, o programa irá requisitar por uma decryption key. Esta foi encontrada realizando um objdump no arquivo encrypt o qual continha a declaração da chave explicitamente no código: "easy". Com isto, é possível decriptar a mensagem.

Os arquivos encrypt_disassembly.txt e encrypt_key_dump.txt contêm o output do objdump realizado para encontrar a chave. A chave fica explícita no arquivo encrypt_key_dump.txt.
