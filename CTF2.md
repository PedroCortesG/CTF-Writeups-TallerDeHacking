### pubcrypt
Lo primero que hice fue visitar la pagina de la que se saco el pulso, pero no pude encontrar el de la fecha exacta ya que no la sabia. No se me ocurrio ver los metadatos entonces pedi la pista1, con lo que consegui la fecha para la key. Con esta (realmente estas, ya que probe con la hora 0:05 y 0:06), hice el xor de bytes (primero se me fue hacer encode a la key, pero despues me di cuenta) e hice print al resultado. Daba cualquier cosa ya que era en bytes, me demore en darme cuenta que tenia que hacer un odt con esos bytes y despues lo abri con libreoffice, obteniendo la flag. Codigo:
```python
def xor_two_bytes(a, b):
    return bytes([a[i % len(a)] ^ b[i % (len(b))] for i in range(max(len(a), len(b)))])
    
if __name__ == "__main__":
    random_key = "9fd940451bec5bb3ac6a356bad9a3b414368a702ee347dfebaa12a2341a99c8b73c3a8aa984cf8d32a705075defe63e4e414c6776d88f2e55ef3d134ef05ddb0"
    with open(r"c:\Users\Pedro\Desktop\pubcrypt.enc", "rb") as f:
        encrypted_bytes = f.read()
        decrypted_bytes = xor_two_bytes(random_key.encode(), encrypted_bytes)
        with open("pubcrypt_decoded.odt", "wb") as g:
            g.write(decrypted_bytes)
```
