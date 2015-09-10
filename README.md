# SINESP API

Função para plataforma AWS Lambda para realizar a consulta de placas de veículos na base de dados do SINESP.

**Como funciona**

Faça uma chamada passando uma placa no formato AAAA1234 e a função faz a pesquisa no serviço SOAP do SINESP e retorna os dados do veículo.

Na resposta, estão incluídas as seguintes informações:
- situacao: Se o veículo possui algum tipo de restrição (roubo, furto, apreensão, etc)
- modelo: Modelo do veículo
- fabricante: Fabricante do veículo
- cor: Cor do veículo
- ano: Ano de fabricação do veículo
- anoModelo: Ano do modelo do veículo
- uf: UF onde a placa está registrada
- municipio: Cidade onde a placa está registrada
- chassi: Últimos 5 dígitos do chassi do veículo

O formato de retorno da API é em JSON.

**Faça seus próprios testes**

Para testar a função em ambiente de desenvolvimento local, utilize [node-lambda](https://github.com/rebelmail/node-lambda).