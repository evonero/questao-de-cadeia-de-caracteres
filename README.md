# questao-de-cadeia-de-caracteres
def programa():     
    while True:          
    frase=input('numero: ')         
    nova_frase=''        
        for letra in frase:                            
            if eh_numero(letra):                                                                                                                
                letra=' '+n_extenso(letra)+' '                             
            elif eh_letra(letra):               
                letra=' '+letra+' '              
        nova_frase = nova_frase + letra        
        print(nova_frase) 
        resposta=' '
        while resposta not in 'SN':            
            resposta=str(input('quer continuar?[S/N] ')).upper()        
        if resposta in 'N':             
            break                   
def eh_numero(letra):     
    if letra in '0123456789':        
        return True 
def eh_letra(letra):     
    if ord(letra) in range(65,91) or ord(letra) in range(97,123):        
        return True    
def n_extenso(letra):     
    letra=int(letra)     
    numeros=['um','dois','tres','quatro',     'cinco','seis','sete','oito','nove','zero']    
    numero=numeros[letra-1]   
        return numero                                                             
 programa()
