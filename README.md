# Projeto-Medusa-e-Kali-Linux
Simulando um Ataque de Brute Force de Senhas em serviços FTP com Medusa e Kali Linux (Desafio DIO)

> **AVISO LEGAL E ÉTICO:**
> Este projeto documenta simulações controladas de ataques de força-bruta em ambiente de laboratório. **NUNCA** execute testes contra sistemas que você não possui ou para os quais não tem permissão expressa por escrito. Este repositório destina-se a fins educacionais e de auditoria em ambientes isolados.

## Índice

* [Descrição do Desafio](#descrição-do-desafio)
* [Objetivos de Aprendizagem](#objetivos-de-aprendizagem)
* [Resumo do Trabalho Realizado](#resumo-do-trabalho-realizado)
* [Ambiente de Laboratório](#ambiente-de-laboratório)
* [Cenário Testado](#cenário-testado)
* [Metodologia](#metodologia)
* [Recomendações de Mitigação](#recomendações-de-mitigação)
* [Referências Úteis](#referências-e-leituras-úteis)
* [Contato](#contato)


## Descrição do Desafio

Implementar, documentar e compartilhar um projeto prático utilizando **Kali Linux** e a ferramenta **Medusa** (ou alternativas) em conjunto com ambientes vulneráveis (Metasploitable 2) para simular cenários de ataque de força-bruta em serviços FTP e exercitar medidas de prevenção. O objetivo é demonstrar compreensão técnica e capacidade de documentar processos e recomendações.


## Objetivos de Aprendizagem

* Compreender ataques de força-bruta em serviços FTP
* Usar Kali Linux e ferramentas de auditoria em ambiente controlado.
* Documentar processos técnicos claramente (wordlists simples, comandos utilizados, configurações).
* Identificar vulnerabilidades e propor mitigação eficaz.
* Publicar um repositório GitHub que sirva de portfólio técnico.


## Resumo do Trabalho Realizado

* **Ambiente:** Kali Linux (VM) e Metasploitable 2 (VM) configuradas em VirtualBox com rede host-only.
* **Cenários testados:** FTP (brute-force).
* **Ferramentas usadas:** Medusa (referência), Nmap (varredura de portas/serviços).
* **Resultados principais:** portas abertas, número de contas comprometidas no lab (fictício).
* **Recomendações:** lista de recomendações de mitigação de ataques de força de bruta em serviços ftp.


## Ambiente de Laboratório

**Descrição técnica:**

* VirtualBox (ou VMware) com duas VMs:

  * `kali-labs` — Kali Linux (VM atacante) — snapshots habilitados.
  * `target-vm` — Metasploitable 2 / DVWA (VM alvo) — snapshots habilitados.
* Rede: **Host-only** (isola VMs da internet).

## Cenário Testado

**FTP — Força Bruta** (simulação conceitual)

   * Objetivo: demonstrar como credenciais fracas podem ser exploradas em serviços de FTP em um lab isolado.

> O cenário foi executado **apenas** contra as VMs no laboratório.


## Metodologia

1. Planejamento
2. Preparação do laboratório (criação de VMs, snapshots, isolamento de rede).
3. Execução controlada das simulações.
4. Coleta de métricas e evidências.
5. Análise, documentação e entrega no GitHub.

## Recomendações de Mitigação

* Se possível, migre para SFTP (mais seguro) e desative FTP.
* Ative fail2ban para banir IPs com N tentativas falhas.
* Habilite bloqueio por PAM (pam_faillock) para bloquear contas após tentativas repetidas.
* Desabilite anônimo, use chroot, e faixa de portas passivas + TLS se continuar com FTP.
* Configure firewall para rate limiting e, se possível, allowlist ou VPN para acesso.
* Configure monitoramento/alertas sobre falhas de autenticação.

## Referências e leituras úteis

* [Kali Linux — site oficial](https://www.kali.org/)
* [Medusa — documentação oficial](http://foofus.net/goons/jmk/medusa/medusa.html)
* [Nmap — manual oficial](https://nmap.org/book/)
* [OWASP Authentication Cheat Sheet (práticas de defesa)](https://cheatsheetseries.owasp.org/cheatsheets/Authentication_Cheat_Sheet.html)

## Contato

* Autor: Rafael Kmohan Paulino Patricio
* Email: <rkmohanpp@gmail.com>
* Repositório: <https://github.com/r121990/Projeto-medusa-kali-ftp>
