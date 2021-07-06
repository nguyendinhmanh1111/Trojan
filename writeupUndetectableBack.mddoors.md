1. Create a payload using msfvenom using the command
2. Pass this through a simple python script that will run the XOR encryption through this output and spits out the encrypted version of the shellcode. 
3. Run "XORencryption.py" to pass the raw payload and output the XOR encrypted payload
python xor_encryptor.py raw.txt > xor_output.txt
