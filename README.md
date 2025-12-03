# 🎣 Phishing com Social Engineering Toolkit (SET)

## 📋 Descrição do Desafio
Este projeto consiste na criação de uma página falsa do Facebook utilizando o **Social Engineering Toolkit (SET)** no Kali Linux. O objetivo é demonstrar como ataques de phishing funcionam tecnicamente para capturar credenciais e, com base nisso, conscientizar sobre métodos de prevenção.

*Nota: Este projeto foi realizado em ambiente controlado (laboratório virtual) para fins estritamente educacionais.*

## 🛠️ Ferramentas Utilizadas
* **Kali Linux:** Sistema operacional ofensivo.
* **setoolkit:** Ferramenta de automação de ataques de engenharia social.
* **Terminal:** Para execução dos comandos e visualização das credenciais capturadas.

## ⚙️ Passo a Passo da Execução

1.  **Acesso ao Root:** O comando `sudo su` foi utilizado para garantir permissões administrativas.
2.  **Início do SET:** Execução do comando `setoolkit`.
3.  **Seleção do Vetor:**
    * Menu: `1) Social-Engineering Attacks`
    * Sub-menu: `2) Website Attack Vectors`
    * Método: `3) Credential Harvester Attack Method`
    * Ação: `2) Site Cloner`
4.  **Configuração:**
    * IP do Atacante: Definido como o IP da máquina Kali (ex: `192.168.x.x`).
    * URL Alvo: `www.facebook.com`.
5.  **Captura:** O SET clona a página de login do Facebook e inicia um servidor Apache local. Quando a "vítima" acessa o IP do atacante, a página falsa é exibida. Ao tentar logar, os dados são interceptados e exibidos no terminal do atacante.

## 🛡️ Resultados e Mitigação

### O que acontece no ataque?
O usuário acredita estar no site legítimo, mas ao observar a **URL**, nota-se que é um endereço IP ou um domínio estranho, não o `facebook.com` oficial. As credenciais digitadas são enviadas em texto claro para o atacante antes de redirecionar a vítima para a página real (para diminuir a suspeita).

### Como se prevenir?
1.  **Verifique a URL:** Sempre confira o endereço na barra do navegador antes de digitar senhas.
2.  **Gerenciadores de Senhas:** Eles não preenchem automaticamente os campos se a URL não coincidir com o domínio real gravado.
3.  **2FA (Autenticação de Dois Fatores):** Mesmo que o atacante capture a senha, ele não terá o token do segundo fator (SMS ou App Autenticador).
4.  **Não clique em links suspeitos:** Acesse os serviços digitando o endereço diretamente no navegador.

---
*Projeto desenvolvido para o Bootcamp de Cibersegurança da DIO.*
