# Info

Aplicação node web que aguarda um timeout informado numa variável de ambiente para retornar a requisição
Ideal para testes de timeout

# Como usar

Utilize o docker compose como exemplo. Configure o timeout desejado através da variável de ambiente 'TIMEOUT'.
Caso não informe, assume o timeout default de 60 segundos.
> O tempo do timeout é informado em milissegundos. <br>
> Exemplo: 1 minuto = 60 segundos = 60000 milissegundos, informe o valor de 60000!

Execute o comando docker:

```
docker run -d --rm --name timeout-app \
    -e TIMEOUT=30000 \
    -p 3000:3000 \
    wquintanilhadasilva/timeout-app
```