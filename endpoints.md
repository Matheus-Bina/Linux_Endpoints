# Para começar a testar os endpoints(URL) precisamos do Postman ou usar o Curl no Linux.

Temos estes endpoints para teste todas no metodo GET:
- status.sh -> mostra se o Servidor EC2 esta ligado e funcionando;
- export.sh -> exibe informações sobre a instancia como, quanto tempo esta ligada, quanto de memoria esta consumindo.

(serão adicionados mais em breve)

Algumas das alterações que podem ocorrer é de IP da URL, caso a EC2 seja reiniciada ou desligada, será necessario mudar o endereço IP da URL.

# Status.sh 

URL - GET - http://18.220.65.31/cgi-bin/status.sh

Será inserido esta linha no Postman para ele ter um retorno dos scripts que estão no Linux, deverão retornar algo semelhante a este body:

```text
API ONLINE NO AMAZON LINUX
```

Indicando que o Servidor esta ligado e funcionando normalmente.

# Export.sh 

URL - GET - http://18.220.65.31/cgi-bin/export.sh

Devera retornar exatamente esta estrutura, mas com informações diferentes já que são dados que se alteram diariamente

```json
{
  "host": "ip-172-31-39-102.us-east-2.compute.internal",
  "uptime": "1 week, 14 hours, 34 minutes",
  "disk": "21%",
  "mem_free_mb": "298"
}
```
Será exibido 
- Host (Servidor AWS);
- Tempo que a Instancia esta ligada;
- Quanto do Disco esta sendo utilizado somente para rodar o Linux;
- quantos MegaBytes de mémoria ainda pode ser usado.

