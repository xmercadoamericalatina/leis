# Legislação brasileira — lei seca

Atualização de textos normativos obtidos de fontes oficiais, com prioridade à reforma tributária e à legislação trabalhista. **Não se declara que este repositório contém todo o ordenamento brasileiro ou que todas as fontes estejam atualizadas.**

## Atualizador

Veja [`scripts/lei_seca/README.md`](scripts/lei_seca/README.md) para o funcionamento de cada script, fontes habilitadas, execução, testes e limitações.

- Constituição, EC 132/2023, LC 214/2025, LC 227/2026, CTN, CLT e demais prioridades: reconsulta diária quando a fonte está acessível e a fila é executada.
- Base federal do Senado e APIs SAPL cadastradas: descoberta incremental e rechecagem de documentos existentes.
- GitHub Actions: quatro horários diários configurados, sujeitos à habilitação do workflow e às permissões da branch.
- Originais, SHA-256, versões, falhas e cobertura explícita. Sem chaves pagas de API ou geração de interpretação jurídica.

A coleção mantida pelo novo atualizador fica em **`lei-seca/`**, gerada após execução. Seu índice é `lei-seca/indice.json`; pendências e cobertura ficam ao lado. PDFs sem validação de integralidade não são publicados como texto certificado.

## Exclusões e legado

Não entram doutrina, jurisprudência, julgados, acórdãos, súmulas, pareceres, soluções de consulta ou projetos de lei. Consulte [`ESCOPO_LEI_SECA.md`](ESCOPO_LEI_SECA.md) para as categorias retiradas da branch principal e os limites da revisão do acervo herdado.

O estado original foi preservado na branch [`arquivo/acervo-original-2026-10-26`](https://github.com/xmercadoamericalatina/leis/tree/arquivo/acervo-original-2026-10-26). Os coletores antigos e os relatórios `PROGRESSO.md`, `COBERTURA.md` e `WORKLOG.md` permanecem como histórico técnico; suas contagens não descrevem automaticamente o novo escopo.

O material legal herdado não foi validado integralmente. A fonte oficial deve ser conferida antes de citar. Não há inferência automática de vigência ou eficácia, nem substituição do Diário Oficial.

## Testar e executar

```sh
python3 -I -m unittest discover -s scripts/lei_seca -p 'test_*.py' -v
python3 -I scripts/lei_seca/atualizar.py --mode completo
python3 -I scripts/lei_seca/auditar.py lei-seca
```

Código novo sob a licença MIT do repositório. Textos oficiais mantêm a identificação de sua fonte.
