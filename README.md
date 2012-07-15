# Readme

## Pastas

### v1.0

Vers�o estavel procedural do boletoPHP. Mantida aqui apenas para consulta e acesso r�pido. Antes de integrar isto ao projeto ela deve removida.

### imagens

Copiada do v1.0, ter� que ser revista se ficar� dentro de library e remover imagens n�o utilizadas e alterar a qualidade das mesmas.

### library

Vers�o em desenvolvimento.

### tests

Onde ficam os testes.

### samples

Exemplo do uso do BoletoPHP j� com orienta��o a objeto. Como � um exemplo real, o sample criado aqui deve ter a mesma saida do criado no v1. Exemplo:

        samples/caixa_economica_federal.php         => boleto_cef
        samples/caixa_economica_federal_sigcb.php   => boleto_cef_sigcb.php

Por isso ele deve receber os mesmos parametros do seu equivalente na v1. Aqui seria al�m dos testes automatizados vermos uma vers�o real do projeto rodando.

Esta pasta provavelmente ser� removida, e criada um novo reposit�rio para ela ou a manteremos aqui mesmo. Pensar depois sobre isto.

## Rodando os testes

Basta acessar o diret�rio de testes e rodar o phpunit.

        $ cd /my/BoletoPHP/tests
        $ phpunit .