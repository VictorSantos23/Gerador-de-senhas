# Gerador-de-senhas

Gerador de senhas aleatorias 

#Importação de módulos que usarei para esse sistema

import string as s
from random import SystemRandom as sr

#Para informar a quantidade de caracteres que a senha terá
quant = int(input('Digite a quantidade de caracteres da senha: '))

#Esse é o gerador de senhas
print( ''.join( sr().choices(s.ascii_letters + s.punctuation + s.digits, k=quant)))

print('--------------------------------------------------------')
decisao = int(input('DIGITE:\n(0) Para encerrar\n(1) Para gerar nova senha\n'))

if decisao == 0 or decisao == 1:
    while decisao == 1:
        quant = int(input('Digite a quantidade de caracteres da senha: '))
        print(''.join(sr().choices(s.ascii_letters + s.punctuation + s.digits, k=quant)))
        print('--------------------------------------------------------')
        decisao = int(input('DIGITE:\n(0) Para encerrar\n(1) Para gerar nova senha\n'))

    print('Espero que tenha ajudado!')

else:
    print('ERRO')
