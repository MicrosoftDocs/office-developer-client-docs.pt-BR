---
title: Criar um perfil do Outlook usando MFCMAPI
ms.date: 05/18/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 85581bc7-2d81-46af-8836-adef39c933fc
description: MFCMAPI fornece acesso a repositórios MAPI para facilitar a investigação de problemas do Exchange e o Outlook e para fornecer aos desenvolvedores de suporte para o desenvolvimento de MAPI.
ms.openlocfilehash: 8df9a4c2783829b7f3540046daecb12ce0b6b86a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766717"
---
# <a name="create-an-outlook-profile-using-mfcmapi"></a>Criar um perfil do Outlook usando MFCMAPI

MFCMAPI fornece acesso a repositórios MAPI para facilitar a investigação de problemas do Exchange e o Outlook e para fornecer aos desenvolvedores de suporte para o desenvolvimento de MAPI.

**Aplica-se a**: Office 365 | Outlook | Outlook 2016 
  
Para não-desenvolvedores, é recomendável que você usar a interface de usuário do Outlook para criar perfis para o Exchange 2013.
  
## <a name="configure-an-outlook-profile-using-mfcmapi"></a>Configurar um perfil do Outlook usando MFCMAPI

1. Abra [MFCMAPI](https://mfcmapi.codeplex.com/)e no menu do **perfil** , clique em **Mostrar perfis**. 
    
2. No menu **ações** , clique em **Criar perfil**. 
    
3. Criar um novo nome para o perfil e clique em **Okey**. 
    
4. Com o botão direito no novo perfil e, em seguida, no menu **Serviços** , clique em **Adicionar serviço**. 
    
5. Desmarque a caixa "UI do serviço de exibição" e, em seguida, clique em **Okey**. 
    
6. Clique duas vezes no perfil recém-criado e, em seguida, clique no serviço **MSEMS** . 
    
7. Localize a seção de perfil do Exchange.
    
   This can be difficult in Outlook�s MAPI, since in 2010 and above there is no longer the global profile section. To find the Profile section, find the property PR_EMSMDB_SECTION_UID (0x3D150102). The value will be the GUID of the profile section persisted in binary form, which will be used in the subsequent steps. Você precisará esse valor na etapa 9.
    
8. Clique duas vezes em serviço **MSEMS** . 
    
9. Localize a seção de perfil do **Exchange** usando o UID da etapa 7 e único clique para selecionar a linha. 
    
10. No menu de propriedade, clique em **Propriedades adicionais**. 
    
11. Clique em **Adicionar**e, em seguida, adicione as seguintes propriedades: 
    
    **Para Outlook 2016**: `PR_PROFILE_USER_SMTP_EMAIL_ADDRESS_W (0x6641001F)` e`PR_DISPLAY_NAME_W`
    
    **Para o Outlook para Office 365**: `PR_PROFILE_UNRESOLVED_NAME`, `PR_PROFILE_UNRESOLVED_SERVER`, `PR_ROH_PROXY_SERVER`, `PR_ROH_FLAGS`, `PR_ROH_PROXY_AUTH_SCHEME`, `PR_PROFILE_AUTH_PACKAGE`, e`PR_ROH_PROXY_PRINCIPAL_NAME` 
    
    **Para o Exchange 2013**: `PR_PROFILE_UNRESOLVED_NAME`, `PR_PROFILE_UNRESOLVED_SERVER`, `PR_ROH_PROXY_SERVER`, `PR_ROH_FLAGS`, `PR_ROH_PROXY_AUTH_SCHEME`, e `PR_PROFILE_AUTH_PACKAGE`. 
    
12. Clique **Okey**e, em seguida, configure cada propriedade de acordo com a tabela a seguir, dependendo da versão que você está se conectando. 
    
13. No menu de **sessão** , clique em **Logon e o repositório de exibição**e, em seguida, selecione o perfil (se ainda não esteja selecionado). 
    
### <a name="outlook-2016"></a>Outlook 2016
  
||||
|:-----|:-----|:-----|
|**Property** <br/> |**Tag** <br/> |**Descrição** <br/> |
| PR_PROFILE_USER_SMTP_EMAIL_ADDRESS_W  <br/> |0x6641001F  <br/> |Endereço SMTP do usuário  <br/> |
|PR_DISPLAY_NAME_W  <br/> |0x3001001F  <br/> |O nome de exibição do usuário  <br/> |
|PR_STORE_PROVIDERS  <br/> |0x3D000102  <br/> |Configure o valor dessa propriedade, localizado na seção **EMSMDB** e atualizar o UID correspondente para a propriedade correspondente  <br/> |
   
### <a name="outlook-for-office-365"></a>Outlook para Office 365
  
||||
|:-----|:-----|:-----|
|**Property** <br/> |**Valor** <br/> |**Descrição** <br/> |
|PR_PROFILE_UNRESOLVED_NAME<sup>1</sup> <br/> |alias da caixa de correio  <br/> |O alias para a caixa de correio de destino; Por exemplo, administrador  <br/> |
|PR_PROFILE_UNRESOLVED_SERVER<sup>1</sup> <br/> |id de servidor personalizado  <br/> |O valor recuperado da **descoberta automática**. no formato <guid>@tenant.onmicrosoft.com; Por exemplo, F5FA2827-5978-43cd-8FA8-E07BC3BB5591@contoso.onmicrosoft.com  <br/>  *Nó de descoberta automática* : resposta/conta/protocolo/servidor (EXCH)  <br/> |
|PR_ROH_PROXY_SERVER  <br/> |Outlook.office365.com  <br/> | *Nó de descoberta automática* : resposta/conta/protocolo/servidor (EXPR) <sup>2</sup> <br/> |
|PR_ROH_FLAGS  <br/> |ROHFLAGS_USE_ROH (0X1)  <br/> ROH_FLAGS_USE_SSL (0X2)  <br/>  ROHFLAGS_MUTUAL_AUTH (0X4)  <br/>  ROHFLAGS_HTTP_FIRST_ON_FAST (0X8)  <br/>  ROHFLAGS_HTTP_FIRST_ON_SLOW (0X20)  <br/> |Contém as configurações em um perfil usado pelo Outlook para se conectar ao Microsoft Exchange Server usando uma chamada de procedimento remoto (RPC) sobre HTTP (Hypertext Transfer Protocol). *Nó de descoberta automática* : resposta/conta/protocolo/SSL (EXPR) <sup>2</sup> <br/> |
| PR_ROH_PROXY_AUTH_SCHEME  <br/> | RPC_C_HTTP_AUTHN_SCHEME_BASIC (0X1)  <br/> |Representa o protocolo de autenticação a ser usado para esse perfil de *Nó de descoberta automática* : resposta/conta/protocolo/AuthPackage (EXPR) <sup>2</sup> <br/> |
|PR_PROFILE_AUTH_PACKAGE  <br/> |RPC_C_AUTHN_NONE (0X0)  <br/> |Descreve o esquema de autenticação a ser usado para o *Nó de descoberta automática* do RPC: resposta/conta/protocolo/AuthPackage (EXCH)) <sup>3</sup> <br/> |
|PR_ROH_PROXY_PRINCIPAL_NAME  <br/> |Elemento CertPrincipalName  <br/> |Usado para oferecer suporte a autenticação mútua; Por exemplo, msstd:outlook.com *Nó de descoberta automática* : resposta/conta/protocolo/CertPrincipalName (EXPR)) <sup>2</sup> <br/> |
   
### <a name="exchange-2013"></a>Exchange 2013
  
||||
|:-----|:-----|:-----|
|**Property** <br/> |**Valor** <br/> |**Descrição** <br/> |
|PR_PROFILE_UNRESOLVED_NAME<sup>1</sup> <br/> |alias da caixa de correio  <br/> |O alias para a caixa de correio de destino; Por exemplo, administrador  <br/> |
|PR_PROFILE_UNRESOLVED_SERVER<sup>1</sup> <br/> |id de servidor personalizado  <br/> |O valor recuperado da **descoberta automática**. no formato <guid>@tenant.onmicrosoft.com; Por exemplo, F5FA2827-5978-43cd-8FA8-E07BC3BB5591@contoso.onmicrosoft.com  <br/>  *Nó de descoberta automática* : resposta/conta/protocolo/servidor (EXCH)  <br/> |
|PR_ROH_PROXY_SERVER  <br/> | nome de domínio do servidor de acesso de cliente  <br/> | O nome de domínio totalmente qualificado (FQDN); Por exemplo, e2013cas.contoso.com *Nó de descoberta automática* : resposta/conta/protocolo/servidor (EXPR) <sup>2</sup> <br/> |
|PR_ROH_FLAGS  <br/> |ROHFLAGS_USE_ROH (0X1)  <br/>  ROHFLAGS_HTTP_FIRST_ON_FAST (0X8)  <br/> ROHFLAGS_HTTP_FIRST_ON_SLOW (0X20))  <br/> |Contém as configurações em um perfil usado pelo Outlook para se conectar ao Microsoft Exchange Server usando uma chamada de procedimento remoto (RPC) sobre Hypertext Transfer Protocol (HTTP) *Nó de descoberta automática* : resposta/conta/protocolo/SSL (EXPR) <sup>2</sup> <br/> |
| PR_ROH_PROXY_AUTH_SCHEME  <br/> | RPC_C_HTTP_AUTHN_SCHEME_NTLM (0X2)  <br/> |Representa o protocolo de autenticação a ser usado para esse perfil de *Nó de descoberta automática* : resposta/conta/protocolo/AuthPackage (EXPR) <sup>2</sup> <br/> |
|PR_PROFILE_AUTH_PACKAGE  <br/> |RPC_C_AUTHN_WINNT (0XA)  <br/> |Descreve o esquema de autenticação a ser usado para RPC *Nó de descoberta automática* : resposta/conta/protocolo/AuthPackage (EXCH)) <sup>3</sup> <br/> |
   
> [!NOTE] 
> - Todos os valores de propriedade mencionados acima podem variar para sua organização específica. 
> - <sup>1</sup> que você deve usar a versão Unicode, em vez da versão ANSI. 
> - Você deve usar o sem formatação antigo POX (XML) com base em descoberta automática. Esta é a descoberta automática com suporte apenas para configurar perfis do Outlook/Exchange.
> - Você pode usar o Outlook para fazer uma solicitação de descoberta automática em seu nome, clicando no ícone do Outlook na **Bandeja do sistema**, ao mesmo tempo, mantendo pressionada a tecla CTRL e clicando em **Configuração automática de email de teste**. 
> - Para PR_ROH_FLAGS, seu ambiente pode exigir o sinalizador ROHFLAGS_SSL_ONLY (0x2) para informar MAPI para usar apenas SSL. Se seu ambiente requer autenticação mútua, você precisará definir esse sinalizador também [ROHFLAGS_MUTUAL_AUTH (0x4)]. Definindo ROHFLAGS_MUTUAL_AUTH (0x4) exigirá que você também pode definir a propriedade PR_ROH_PROXY_PRINCIPAL_NAME. Você deve definir essa opção para ser o nome principal do servidor.
> - <sup>2</sup> para o Outlook 2010, você precisará usar o protocolo EXPR. Outlook 2013 usa o protocolo EXHTTP. 
> - <sup>3</sup> este valor não pode ser na resposta da descoberta automática. Se não especificado, o cliente deve usar Kerberos ou NTLM. 
    
Para obter dicas de solução de problemas, consulte [como configurar um perfil do Outlook usando MFCMAPI para o Exchange 2013](https://blogs.msdn.microsoft.com/dvespa/2014/01/16/how-to-configure-an-outlook-profile-using-mfcmapi-for-exchange-2013).
  
## <a name="see-also"></a>Confira também

- [Referência de MAPI do Outlook](https://msdn.microsoft.com/en-us/library/office/cc765775.aspx)  
- [Criar programaticamente um perfil no Outlook](https://msdn.microsoft.com/en-us/library/office/mt707568.aspx)
    

