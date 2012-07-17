# Readme

## Contribuindo

Este � o modo que venho fazendo, e para o sucesso do projeto, pelo menos neste inicio enquanto estamos em um feature branch algumas coisas feias devem ser feitas =/

### Escolhendo um boleto

Abra a pasta <code>v1.0</code> e selecione um boleto que ainda n�o foi implementado em <code>library/BoletoPHP/Boletos/</code>.

### Criando o nova implementa��o do boleto

Crie uma classe em <code>library/BoletoPHP/Boletos/</code> com o nome do boleto sempre em upper CamelCase, assim como o nome do arquivo. Copie o arquivo <code>CaixaEconomicaFederal.php</code> e trabalhe a partir dele.

### Criando o teste

Em <code>tests/library/BoletoPHP/Boletos/</code> crie um arquivo de teste copiando o do <code>CaixaEconomicaFederalTest.php</code> e trabalhe a partir dele

No arquivo de test passe para os parametros os mesmos valores passados pelo boleto do v1.0.

### Alguns padr�es

J� vimos como nomear os arquivos e classes.

M�todos nomeados em lower camelCase.

Defina sempre a visibilidade dos m�todos e atributos para a mais restrita possivel.

Nada de <code>_</code> ou <code>__</code> para dizer se um m�todo � privado ou protected para isso temos os declaradores de visibilidade.

Agora vem a parte mais feia que falei =/, nos m�todos que por um acaso tivermos que copiar do v1.0 como o https://github.com/maurogeorge/boletophp/blob/refactory-oop/library/BoletoPHP/Boletos/Boleto.php#L237 manter a mesma nomenclatura e implementa��o, por mais feia que seja nos ajudara a encontrar seu equivalente no v1.0 se for necess�rio. Claro que antes de integrarmos tudo no master, iremos nomear tudo para nomes mais bonitos e de acordo com o padr�o, al�m de refatorar S2.

### Observa��o

Legal sempre seguirmos a https://github.com/php-fig/fig-standards.

### Mais como faz?

1 Fa�a um Fork
2 Crie seu feature branch (git checkout -b my-new-feature)
3 Commit suas mudan�as (git commit -am 'Added some feature')
4 De push para o seu branch (git push origin my-new-feature)
5 Crie um pull Request

### Pastas

#### v1.0

Vers�o estavel procedural do boletoPHP. Mantida aqui apenas para consulta e acesso r�pido. Antes de integrar isto ao projeto ela deve removida.

#### imagens

Copiada do v1.0, ter� que ser revista se ficar� dentro de library e remover imagens n�o utilizadas e alterar a qualidade das mesmas.

#### library

Vers�o em desenvolvimento.

#### tests

Onde ficam os testes.

#### samples

Exemplo do uso do BoletoPHP j� com orienta��o a objeto. Como � um exemplo real, o sample criado aqui deve ter a mesma saida do criado no v1. Exemplo:

        samples/caixa_economica_federal.php         => boleto_cef
        samples/caixa_economica_federal_sigcb.php   => boleto_cef_sigcb.php

Por isso ele deve receber os mesmos parametros do seu equivalente na v1. Aqui seria al�m dos testes automatizados vermos uma vers�o real do projeto rodando.

Esta pasta provavelmente ser� removida, e criada um novo reposit�rio para ela ou a manteremos aqui mesmo. Pensar depois sobre isto.

## Rodando os testes

Basta acessar o diret�rio de testes e rodar o phpunit.

        $ cd /my/BoletoPHP/tests
        $ phpunit .