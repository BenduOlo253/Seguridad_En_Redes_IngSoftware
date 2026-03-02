# Descripción.
Can you read files in the root file?The system admin has provisioned an account for you on the main server:`ssh -p 60448 picoplayer@saturn.picoctf.net`Password: `33qE7mB5BF`Can you login and read the root file?
**Pistas:**
1. What permissions do you have?
# Solución.
1. Ingrese a la ruta.
2. Verifique lo que puedo ejecutar con sudo -l
3. Puedo ejecutar vi.
4. Dentro de vi ejecute este comando:
   :!/bin/sh
5. Ya que herede los permisos del root explore la carpeta challenge/.
6. explore los documentos dentro de challenge.
7. hice un cat al unico documento que había y encontre la bandera.
**Flag: picoCTF{uS1ng_v1m_3dit0r_3dd6dcf4}**
# Notas Adicionales.
el uso de vim es sumamente intersante, el como puedo heredar los permisos de root.
# Referencias.
pedi ayuda a gemini.
