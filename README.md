<p align="center"><img src="assets/xmercado-hellenai-base-legal.svg" alt="XMERCADO e HELLENAI — Base Legal" width="100%"></p>

<h1 align="center">XMERCADO × HELLENAI · Base Legal</h1>

<p align="center"><strong>Legislação brasileira com origem identificada, histórico de versões e atualização automatizada.</strong></p>

<p align="center">
<a href="https://www.xmercado.com.br">XMERCADO</a> ·
<a href="https://hellenai.com.br">HELLENAI</a> ·
<a href="https://github.com/xmercadoamericalatina/leis/actions">Coletas e execuções</a> ·
<a href="scripts/lei_seca/README.md">Documentação</a>
</p>

---

## Nossa base legal

Uma iniciativa **XMERCADO e HELLENAI** para organizar e manter uma base de lei seca obtida de fontes oficiais. A identidade desta edição, sua apresentação e a manutenção do atualizador são conduzidas pela XMERCADO e HELLENAI.

| Princípio | Aplicação |
| --- | --- |
| Fonte oficial | Origem identificada em cada documento coletado. |
| Lei seca | Sem doutrina, comentários ou conteúdo jurisprudencial nas novas coletas. |
| Rastreabilidade | Originais, hashes SHA-256 e versões preservadas. |
| Transparência | Cobertura, falhas e pendências registradas. |

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

## Origem, autoria e licença

Esta edição é um fork de [ctresb/leis](https://github.com/ctresb/leis). Reconhecemos a contribuição do projeto original e de seus autores. A identidade XMERCADO e HELLENAI identifica a manutenção e a evolução desta edição; não atribui à empresa a autoria das contribuições anteriores ou dos textos oficiais.

Os avisos de copyright, a [licença original](LICENSE) e o histórico de contribuições são preservados. A indicação “forked from” exibida pelo GitHub registra essa origem e não é removida por uma mudança visual.

---

<p align="center"><strong>XMERCADO × HELLENAI</strong><br>Informação legal com fonte, histórico e transparência.</p>
