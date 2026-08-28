# Portfólio — Eric Luan

Portfólio pessoal de **Eric Luan**, Analista de Suporte e Infraestrutura.
Uma página única, estática, escura, construída para carregar rápido e
funcionar em qualquer lugar — sem framework, sem build, sem dependência
de servidor.

> **Infraestrutura que fica de pé. Suporte que resolve.**

---

## Sobre o projeto

A ideia era ter um lugar próprio para apresentar trajetória, stack e
automações — algo mais direto que um PDF de currículo e mais meu que um
perfil de rede social. O resultado é um único `index.html` que pode ser
hospedado no GitHub Pages, num bucket S3 ou aberto direto do disco.

A página é organizada em cinco seções numeradas:

| # | Seção | Conteúdo |
|---|-------|----------|
| 01 | **Stack** | Ferramentas do dia a dia — Windows Server, Linux/RHEL, Active Directory, Azure, AWS, redes, Zabbix/Grafana, PowerShell/Python, Jira, backup e endpoint |
| 02 | **Experiência** | Linha do tempo profissional, de help desk a suporte e infraestrutura |
| 03 | **Projetos** | Cinco repositórios de automação nascidos de problemas reais de operação |
| 04 | **Formação** | Graduação em Ciência da Computação e certificações em cloud, Linux, redes e automação |
| 05 | **Contato** | E-mail, GitHub e LinkedIn |

Os projetos em destaque, todos com repositório próprio:

- [`intune-automation`](https://github.com/ericluanz/intune-automation) — empacotamento e distribuição de apps via Microsoft Intune
- [`m365-powershell-toolkit`](https://github.com/ericluanz/m365-powershell-toolkit) — administração do Microsoft 365 e Exchange
- [`powershell-automation`](https://github.com/ericluanz/powershell-automation) — provisionamento de um domínio Active Directory em oito etapas
- [`python-automation`](https://github.com/ericluanz/python-automation) — rotinas de infraestrutura em Python
- [`samba-automation`](https://github.com/ericluanz/samba-automation) — gerenciador de servidores de arquivos Samba em Debian/Ubuntu

---

## O que tem por baixo

**Cena 3D reativa ao scroll.** O fundo é uma placa-mãe montada
proceduralmente em [three.js](https://threejs.org/) — PCB, dissipadores,
slots, trilhas e LEDs. Conforme a página rola, a placa gira e as peças se
afastam num efeito de vista explodida, com a câmera acompanhando. Nada é
carregado de um arquivo `.glb`: a geometria toda é construída em código.

**Bilíngue (PT/EN).** Um dicionário `I18N` alimenta os atributos
`data-i18n` do HTML; o botão no topo troca o idioma sem recarregar a
página, e a escolha fica salva no `localStorage`.

**Revelação progressiva.** Um `IntersectionObserver` anima cada bloco na
entrada da viewport, com fallback por evento de scroll para o que já está
acima da dobra.

**Detalhes de acabamento.** Metadados Open Graph e Twitter Card para
preview em LinkedIn, WhatsApp e Slack; respeito a
`prefers-reduced-motion`; layout responsivo; tipografia Space Grotesk +
JetBrains Mono.

### Stack

- HTML, CSS e JavaScript puros — **sem build, sem `node_modules`**
- three.js `0.152.2` via CDN
- Google Fonts

---

## Rodando localmente

```bash
git clone https://github.com/ericluanz/meu-portifolio.git
cd meu-portifolio
```

Abra o `index.html` no navegador. Só isso.

Se preferir servir por HTTP (útil para testar o preview dos metadados):

```bash
python -m http.server 8000
# http://localhost:8000
```

---

## Sobre o uso do Claude

Este projeto foi desenvolvido em par com o **Claude** (Anthropic), usando
o Claude Code no terminal. Vale registrar isso abertamente, porque a forma
de trabalho fez diferença no resultado.

O que veio de mim: a decisão do que a página precisava comunicar, o
conteúdo (trajetória, stack, projetos, textos), a direção visual — dark,
técnico, sem excesso — e o julgamento de cada iteração. Várias versões
foram descartadas no caminho até chegar na estética atual.

O que o Claude acelerou: a construção da cena em three.js, que teria sido
a parte mais demorada de escrever à mão; o sistema de i18n; o ajuste fino
de CSS em cima de feedback do tipo *"o hero está pesado demais"*; e a
revisão de detalhes fáceis de esquecer, como os metadados Open Graph e o
`.gitignore` que mantém os backups locais fora do repositório público.

O fluxo foi conversacional e iterativo: eu descrevia o que queria ou o que
estava errado, o Claude propunha a mudança no arquivo, eu olhava o
resultado no navegador e pedia o próximo ajuste. Nenhuma linha entrou sem
passar por essa checagem.

Não acho que isso diminua o projeto — é a mesma lógica que aplico em
infraestrutura: automatizar o trabalho repetitivo para gastar o tempo onde
ele realmente rende. A ferramenta mudou; o critério sobre o que é um bom
resultado continua sendo meu.

---

## Contato

- **E-mail** — [ericluan345@gmail.com](mailto:ericluan345@gmail.com)
- **GitHub** — [@ericluanz](https://github.com/ericluanz)
- **LinkedIn** — [in/ericluanz](https://www.linkedin.com/in/ericluanz/)
