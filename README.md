# Prova digital: o protocolo comprova o quê?

Uma cliente contesta uma cobrança no portal da empresa. Envia o pedido e dois anexos. O portal gera o protocolo `1042`, mas só confirma o recebimento de um dos arquivos. **A cliente não precisa estar em litígio para querer saber se o pedido chegou completo.**

```python
anexos_do_pedido = {"fatura.pdf", "comprovante.pdf"}
anexos_confirmados = {"fatura.pdf"}  # conforme o recibo do portal

sem_confirmacao = anexos_do_pedido - anexos_confirmados
print(sorted(sem_confirmacao))  # ['comprovante.pdf']
```

1. **Código.** Compara o que a cliente tentou enviar com o que o portal confirmou. É um teste do recibo, não uma perícia.

2. **Resultado.** O número identifica a solicitação, mas não confirma o recebimento de `comprovante.pdf`. Isso não prova que o arquivo se perdeu. Prova apenas que o recibo não esclarece essa parte do envio.

3. **Fundamento.** Na **administração pública**, o [art. 8º da Lei de Governo Digital](https://www2.camara.leg.br/legin/fed/lei/2021/lei-14129-29-marco-2021-791203-normaatualizada-pl.html) prevê recibo eletrônico que identifique o ato processual, considerado realizado na data e hora do recebimento pelo sistema. Nas **empresas**, o [art. 12 do Decreto nº 11.034/2022](https://www2.camara.leg.br/legin/fed/decret/2022/decreto-11034-5-abril-2022-792480-publicacaooriginal-164911-pe.html) garante acompanhamento e acesso ao histórico nos SACs de fornecedores de serviços regulados pelo Executivo federal. Não é uma regra geral para todo atendimento privado.

4. **Decisão do gestor.** Emitir recibo após registrar o pedido, informar quais anexos foram aceitos ou rejeitados e manter um histórico acessível. Assim, o requerente pode corrigir uma pendência antes do prazo, sem começar o atendimento do zero.

5. **Atuação do advogado digital.** Traduzir a regra aplicável em um teste com a equipe de produto: **se um anexo falhar, o portal avisa ou registra tudo como recebido?** Definir também quem pode consultar o histórico, por quanto tempo ele é necessário e como proteger os dados pessoais ali registrados.

**Prova digital não começa no processo judicial. Começa quando o sistema permite ao requerente verificar o que foi recebido e acompanhar o que aconteceu depois.**
