# Bem-vindo ao projeto


## Documentação útil


## Projeto Automação API
Foi Desenvolvida uma automação de testes para a API utilizando Rest-Assured.
* URL utilizada: https://viacep.com.br/ws/91060900/json/ 

#### Cenários:
```
* Cenário: Consulta CEP valido
Dado que o usuário inseri um CEP válido
Quando o serviço é consultado
Então é retornado o CEP, logradouro, complemento, bairro, localidade, uf e ibge.

* Cenário: Consulta CEP inexistente
Dado que o usuário inseri um CEP que não exista na base dos Correios
Quando o serviço é consultado 
Então é retornada um atributo erro

* Cenário: Consulta CEP com formato inválido 
Dado que o usuário inseri um CEP com formato inválido
Quando o serviço é consultado 
Então é retornado uma mensagem de erro

* Extras:
1)	Criar um cenário que verifique o retorno do serviço abaixo:
URL: https://viacep.com.br/ws/RS/Gravatai/Barroso/json/
```


#### Estruturação do Projeto:
```
├── ViaCepAPI                                         # Projeto                                                                                          
    ├── src/main/java                                 #                                                                                                         
        ├── br.df.lseabra.core                        # Pacote de Core                                                                                        
            ├── BaseTest.java                         # classe que será extendida pelas classes de teste
            ├── Constantes.java                       # Interface contendo porta, Url e Content type
        ├── br.df.lseabra.test                        # Pacote de Testes
            ├── RConsultasTest.java                   #Classe com testes com os cenários + Extra

```

#### Executar o Teste
Executar pela IDE de sua preferência os arquivos: 
```
ConsultasTest.java                                     # Suite de teste para quando há login de cliente ao entrar no site
```

#### Execução dos testes:
![image](https://user-images.githubusercontent.com/49051123/116837944-d619d180-aba2-11eb-8859-4ab02126e08d.png)


#### Tecnologia:

Tecnologias utilizadas no projeto:
  * JRE 1.8.0_281
  * Maven
  * io.rest-assured 4.0.0 
  * groovy 3.0.5
  * Eclipse

