---
title: Criar um perfil do Outlook usando MFCMAPI
ms.date: 05/18/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 85581bc7-2d81-46af-8836-adef39c933fc
description: MFCMAPI fornece acesso às lojas MAPI para facilitar a investigação de problemas do Exchange e do Outlook e para fornecer suporte a desenvolvedores para o desenvolvimento de MAPI.
ms.openlocfilehash: 8a300ad53918b22cc3de5554a1e3c29289cd9365
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397874"
---
# <a name="create-an-outlook-profile-using-mfcmapi"></a>Criar um perfil do Outlook usando MFCMAPI

MFCMAPI fornece acesso às lojas MAPI para facilitar a investigação de problemas do Exchange e do Outlook e para fornecer suporte a desenvolvedores para o desenvolvimento de MAPI.

**Aplica-se a**: Office 365 | Outlook | Outlook 2016 
  
Para não desenvolvedores, é recomendável usar a interface de usuário do Outlook para criar perfis para o Exchange 2013.
  
## <a name="configure-an-outlook-profile-using-mfcmapi"></a>Configurar um perfil do Outlook usando MFCMAPI

1. Abra [MFCMAPI](https://mfcmapi.codeplex.com/)e, no menu **Perfil**, clique em **Exibir perfis**. 
    
2. No menu **Ações**, clique em **Criar perfil**. 
    
3. Crie um novo nome para o perfil e depois clique em **OK**. 
    
4. Clique com botão direito novo perfil e, em seguida, no menu **Serviços**, clique em **Adicionar serviço**. 
    
5. Desmarque a caixa "Exibir serviço de interface do usuário e, em seguida, clique em **OK**. 
    
6. Clique duas vezes no perfil recém-criado e clique no serviço **MSEMS**. 
    
7. Localize a seção do Perfil do Exchange.
    
   Isso pode ser difícil no MAPI do Outlook porque, em 2010 e depois disso, não existe mais a seção de perfil global. To find the Profile section, find the property PR_EMSMDB_SECTION_UID (0x3D150102). O valor será o GUID da seção perfil persistente no formato binário, que será usado nas etapas subsequentes. Esse valor será necessário na etapa 9.
    
8. Clique duas vezes no serviço **MSEMS**. 
    
9. Localize a seção de perfil do **Exchange** usando a UID da etapa 7 e, em seguida, clique uma vez para selecionar a linha. 
    
10. No menu Propriedades, clique em **Propriedades adicionais**. 
    
11. Clique em **Adicionar**e adicione as seguintes propriedades: 
    
    **No Outlook 2016**: `PR_PROFILE_USER_SMTP_EMAIL_ADDRESS_W (0x6641001F)` e `PR_DISPLAY_NAME_W`
    
    **No Outlook para Office 365**: `PR_PROFILE_UNRESOLVED_NAME`, `PR_PROFILE_UNRESOLVED_SERVER`, `PR_ROH_PROXY_SERVER`, `PR_ROH_FLAGS`, `PR_ROH_PROXY_AUTH_SCHEME`, `PR_PROFILE_AUTH_PACKAGE` e `PR_ROH_PROXY_PRINCIPAL_NAME` 
    
    **Para o Exchange 2013**: `PR_PROFILE_UNRESOLVED_NAME`, `PR_PROFILE_UNRESOLVED_SERVER`, `PR_ROH_PROXY_SERVER`, `PR_ROH_FLAGS`, `PR_ROH_PROXY_AUTH_SCHEME` e `PR_PROFILE_AUTH_PACKAGE`. 
    
12. Clique em **OK** e depois configure cada propriedade de acordo com a tabela a seguir, dependendo da versão à qual você está se conectando. 
    
13. No menu **Seção**, clique em **Logon e exibir loja** e depois selecione o perfil (se já não estiver selecionado). 
    
### <a name="outlook-2016"></a>Outlook 2016
  
||||
|:-----|:-----|:-----|
|**Propriedade** <br/> |**Tag** <br/> |**Descrição** <br/> |
| PR_PROFILE_USER_SMTP_EMAIL_ADDRESS_W  <br/> |0x6641001F  <br/> |Endereço SMTP do usuário  <br/> |
|PR_DISPLAY_NAME_W  <br/> |0x3001001F  <br/> |O nome de exibição do usuário.  <br/> |
|PR_STORE_PROVIDERS  <br/> |0x3D000102  <br/> |Configure o valor dessa propriedade, localizado na seção **EMSMDB** e atualizar a UID correspondente da propriedade correspondente  <br/> |
   
### <a name="outlook-for-office-365"></a>Outlook para Office 365
  
||||
|:-----|:-----|:-----|
|**Propriedade** <br/> |**Valor** <br/> |**Descrição** <br/> |
|PR_PROFILE_UNRESOLVED_NAME<sup>1</sup> <br/> |alias da caixa de correio  <br/> |O alias da caixa de correio de destino; como Administrador  <br/> |
|PR_PROFILE_UNRESOLVED_SERVER<sup>1</sup> <br/> |id do servidor personalizado  <br/> |Valor recuperado da **Descoberta Automática**. no formato <guid>@tenant.onmicrosoft.com; por exemplo, F5FA2827-5978-43cd-8FA8-E07BC3BB5591@contoso.onmicrosoft.com  <br/>  *Nó de Descoberta Automática* : resposta/conta/protocolo/servidor (Exchange)  <br/> |
|PR_ROH_PROXY_SERVER  <br/> |outlook.office365.com  <br/> | *Nó de Descoberta Automática* : resposta/conta/protocolo/servidor (EXPR) <sup>2</sup> <br/> |
|PR_ROH_FLAGS  <br/> |ROHFLAGS_USE_ROH (0X1)  <br/> ROH_FLAGS_USE_SSL (0X2)  <br/>  ROHFLAGS_MUTUAL_AUTH (0X4)  <br/>  ROHFLAGS_HTTP_FIRST_ON_FAST (0X8)  <br/>  ROHFLAGS_HTTP_FIRST_ON_SLOW (0X20)  <br/> |Contém as configurações em um perfil usado pelo Outlook para se conectar ao Microsoft Exchange Server usando uma chamada de procedimento remoto (RPC) sobre protocolo HTTP (Hypertext Transfer). *Nó de Descoberta Automática* : resposta/conta/protocolo/SSL (EXPR) <sup>2</sup> <br/> |
| PR_ROH_PROXY_AUTH_SCHEME  <br/> | RPC_C_HTTP_AUTHN_SCHEME_BASIC (0X1)  <br/> |Representa o protocolo de autenticação a ser usado para este perfil *Nó de Descoberta Automática* : resposta/conta/protocolo/AuthPackage (EXPR) <sup>2</sup> <br/> |
|PR_PROFILE_AUTH_PACKAGE  <br/> |RPC_C_AUTHN_NONE (0X0)  <br/> |Descreve o esquema de autenticação para o *Nó de Descoberta Automática* da RPC: resposta/conta/protocolo/AuthPackage (Exchange)) <sup>3</sup> <br/> |
|PR_ROH_PROXY_PRINCIPAL_NAME  <br/> |Elemento CertPrincipalName  <br/> |Usado para dar suporte à autenticação comum; por exemplo, msstd:outlook.com *Nó de Descoberta Automática* : resposta/conta/protocolo/CertPrincipalName (EXPR)) <sup>2</sup> <br/> |
   
### <a name="exchange-2013"></a>Exchange 2013
  
||||
|:-----|:-----|:-----|
|**Propriedade** <br/> |**Valor** <br/> |**Descrição** <br/> |
|PR_PROFILE_UNRESOLVED_NAME<sup>1</sup> <br/> |alias da caixa de correio  <br/> |O alias da caixa de correio de destino; como Administrador  <br/> |
|PR_PROFILE_UNRESOLVED_SERVER<sup>1</sup> <br/> |id do servidor personalizado  <br/> |Valor recuperado da **Descoberta Automática**. no formato <guid>@tenant.onmicrosoft.com; por exemplo, F5FA2827-5978-43cd-8FA8-E07BC3BB5591@contoso.onmicrosoft.com  <br/>  *Nó de Descoberta Automática* : resposta/conta/protocolo/servidor (Exchange)  <br/> |
|PR_ROH_PROXY_SERVER  <br/> | nome de domínio de servidor de acesso do cliente  <br/> | O nome de domínio totalmente qualificado (FQDN);por exemplo, e2013cas.contoso.com *Nó de Descoberta Automática* : resposta/conta/protocolo/servidor (EXPR) <sup>2</sup> <br/> |
|PR_ROH_FLAGS  <br/> |ROHFLAGS_USE_ROH (0X1)  <br/>  ROHFLAGS_HTTP_FIRST_ON_FAST (0X8)  <br/> ROHFLAGS_HTTP_FIRST_ON_SLOW (0X20))  <br/> |Contém configurações em um perfil usado pelo Outlook para se conectar ao Microsoft Exchange Server usando uma chamada de procedimento remoto (RPC) sobre protocolo HTTP (Hypertext Transfer) *Nó de Descoberta Automática* : resposta/conta/protocolo/SSL (EXPR) <sup>2</sup> <br/> |
| PR_ROH_PROXY_AUTH_SCHEME  <br/> | RPC_C_HTTP_AUTHN_SCHEME_NTLM (0X2)  <br/> |Representa o protocolo de autenticação a ser usado para este perfil *Nó de Descoberta Automática* : resposta/conta/protocolo/AuthPackage (EXPR) <sup>2</sup> <br/> |
|PR_PROFILE_AUTH_PACKAGE  <br/> |RPC_C_AUTHN_WINNT (0XA)  <br/> |Descreve o esquema de autenticação a ser usado para o *Nó de Descoberta Automática* da RPC: resposta/conta/protocolo/AuthPackage (Exchange)) <sup>3</sup> <br/> |
   
> [!NOTE] 
> - Todos os valores de propriedade mencionados acima podem variar para sua organização específica. 
> - <sup>1</sup> Você deve usar a versão Unicode, em vez de versão ANSI. 
> - Você deve usar a Descoberta Automática baseada em Plain Old XML (POX). Esta é a única descoberta automática com suporte para configurar os perfis do Exchange/Outlook.
> - Você pode usar o Outlook para criar uma solicitação de Descoberta Automática em seu nome clicando com o botão direito no ícone do Outlook na **Bandeja do Sistema**, mantendo a tecla CTRL pressionada e clicando em **Configuração Automática de Email de Teste**. 
> - Para PR_ROH_FLAGS, seu ambiente pode exigir o sinalizador ROHFLAGS_SSL_ONLY (0x2) ordenar que o MAPI use somente SSL. Se seu ambiente requer autenticação comum, será necessário configurar esse sinalizador e também [ROHFLAGS_MUTUAL_AUTH (0x4)]. A configuração de ROHFLAGS_MUTUAL_AUTH (0x4) exige que você também pode configure a propriedade PR_ROH_PROXY_PRINCIPAL_NAME. Você deve definir essa como o nome principal do servidor.
> - <sup>2</sup> Para o Outlook 2010, você precisará usar o protocolo EXPR. O Outlook 2013 usa o protocolo EXHTTP. 
> - <sup>3</sup> Esse valor não pode ser estar na resposta da Descoberta Automática. Se não for especificado, o cliente deve usar Kerberos ou NTLM. 
    
Para dicas de Solução de Problemas, confira [Como configurar um perfil do Outlook usando o MFCMAPI do Exchange 2013](https://blogs.msdn.microsoft.com/dvespa/2014/01/16/how-to-configure-an-outlook-profile-using-mfcmapi-for-exchange-2013).
  
## <a name="see-also"></a>Confira também

- [Referência de MAPI do Outlook](https://msdn.microsoft.com/library/office/cc765775.aspx)  
- [Criar um perfil no Outlook de forma programática](https://msdn.microsoft.com/library/office/mt707568.aspx)
    

