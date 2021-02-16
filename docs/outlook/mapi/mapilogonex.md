---
title: MAPILogonEx
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPILogonEx
api_type:
- HeaderDef
ms.assetid: 98091e5b-1abd-4814-9c7a-583b420ee11d
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 9f2ec8f0ec00f7314982e9b112415f69901c358c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424116"
---
# <a name="mapilogonex"></a>MAPILogonEx

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Registra um aplicativo cliente em uma sessão com o sistema de mensagens. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapix.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos do cliente  <br/> |
   
```cpp
HRESULT MAPILogonEx(
  ULONG_PTR ulUIParam,
  LPSTR lpszProfileName,
  LPSTR lpszPassword,
  FLAGS flFlags,
  LPMAPISESSION FAR * lppSession
);
```

## <a name="parameters"></a>Parâmetros

 _ulUIParam_
  
> [in] Alça para a janela para a qual a caixa de diálogo de logon é modal. Se nenhuma caixa de diálogo aparecer durante a chamada, o  _parâmetro ulUIParam_ será ignorado. Esse parâmetro pode ser zero. 
    
 _lpszProfileName_
  
> [in] Ponteiro para uma cadeia de caracteres que contém o nome do perfil a ser usado quando o usuário faz o login. Esta cadeia de caracteres é limitada a 64 caracteres.
    
 _lpszPassword_
  
> [in] Ponteiro para uma cadeia de caracteres que contém a senha do perfil. O  _parâmetro lpszPassword_ deve ser NULL. 
    
 _flFlags_
  
> [in] Bitmask de sinalizadores usados para controlar como o logon é realizado. Os sinalizadores a seguir podem ser definidos:
    
MAPI_ALLOW_OTHERS 
  
> A sessão compartilhada deve ser retornada, o que permite que clientes posteriores obtenham a sessão sem fornecer nenhuma credencial de usuário. 
    
MAPI_BG_SESSION
  
> Faça logon em uma sessão e execute qualquer operação em segundo plano. Em geral, se um cliente pretende fazer o processamento em um thread em segundo plano ou em um processo separado de uma maneira que seja discreta para o thread em primeiro plano, ele deverá chamar com o sinalizador MAPI_BG_SESSION pesquisa. Um aplicativo cliente como um mecanismo de indexação ou a abertura de um Arquivo de Pastas Particulares (PST) para acesso de tipo em segundo plano são alguns exemplos de onde usar MAPI_BG_SESSION. MAPILogonEx.
    
MAPI_EXPLICIT_PROFILE 
  
> O perfil padrão não deve ser usado e o usuário deve ser obrigado a fornecer um perfil. 
    
MAPI_EXTENDED 
  
> Faça logoff com recursos estendidos. Esse sinalizador sempre deve ser definido.
    
MAPI_FORCE_DOWNLOAD 
  
> Uma tentativa deve ser feita para baixar todas as mensagens do usuário antes de retornar. Se o MAPI_FORCE_DOWNLOAD sinalizador não estiver definido, as mensagens poderão ser baixadas em segundo plano depois que a chamada para MAPILogonEx retornar. 
    
MAPI_LOGON_UI 
  
> Uma caixa de diálogo deve ser exibida para solicitar ao usuário informações de logon, se necessário. Quando o MAPI_LOGON_UI não estiver definido, o cliente de chamada não exibirá uma caixa de diálogo de logon e retornará um valor de erro se o usuário não estiver conectado.
    
MAPI_NEW_SESSION 
  
> Deve ser feita uma tentativa de criar uma nova sessão MAPI em vez de adquirir a sessão compartilhada. Se o MAPI_NEW_SESSION sinalizador não estiver definido, MAPILogonEx usará uma sessão compartilhada existente, mesmo se o parâmetro  _lpszprofileName_ não for NULL. 
    
MAPI_NO_MAIL 
  
> O MAPI não deve informar o spooler MAPI sobre a existência da sessão. O resultado é que nenhuma mensagem pode ser enviada ou recebida na sessão, exceto por meio de um par de armazenamento e transporte fortemente emparelhados. Um cliente de chamada define esse sinalizador se estiver agindo como um agente, se o trabalho de configuração tiver que ser feito ou se o cliente estiver navegando nos armazenamentos de mensagens disponíveis. 
    
MAPI_NT_SERVICE 
  
> O chamador está sendo executado como um serviço do Windows. Os chamadores que não estão sendo executados como um serviço do Windows não devem definir esse sinalizador; os chamadores que estão sendo executados como um serviço devem definir esse sinalizador. 
    
MAPI_SERVICE_UI_ALWAYS 
  
> MAPILogonEx deve exibir uma caixa de diálogo de configuração para cada serviço de mensagem no perfil. As caixas de diálogo são exibidas após o perfil ter sido escolhido, mas antes de qualquer serviço de mensagens estar conectado. A caixa de diálogo comum MAPI para logon também contém uma caixa de seleção que solicita a mesma operação. 
    
MAPI_TIMEOUT_SHORT 
  
> O logon deve falhar se for bloqueado por mais de alguns segundos. 
    
MAPI_UNICODE 
  
> As cadeias de caracteres passadas estão no formato Unicode. Se o MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI. 
    
MAPI_USE_DEFAULT 
  
> O subsistema de mensagens deve substituir o nome de perfil do perfil padrão pelo _parâmetro lpszProfileName._ O MAPI_EXPLICIT_PROFILE sinalizador é ignorado, a menos que  _lpszProfileName_ seja NULL ou vazio. 
    
 _lppSession_
  
> [out] Ponteiro para um ponteiro para a interface de sessão MAPI.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O logon foi bem-sucedido.
    
MAPI_E_LOGON_FAILED 
  
> O logon não foi bem-sucedido, porque um ou mais parâmetros para MAPILogonEx eram inválidos ou porque já havia muitas sessões abertas.
    
MAPI_E_TIMEOUT 
  
> O MAPI serializa todos os logons por meio de um mutex. Isso será retornado se o MAPI_TIMEOUT_SHORT sinalizador tiver sido definido e outro thread tiver mantido o mutex. 
    
MAPI_E_USER_CANCEL 
  
> O usuário cancelou a operação, normalmente clicando no botão Cancelar **em** uma caixa de diálogo. 
    
## <a name="remarks"></a>Comentários

Os aplicativos cliente MAPI chamam a função MAPILogonEx para fazer logon em uma sessão com o sistema de mensagens. Todas as cadeias de caracteres que são passadas e retornadas de e para chamadas MAPI são terminadas por caractere nulo e devem ser especificadas no conjunto de caracteres atual ou na página de código do cliente ou do sistema operacional do provedor de chamada.
  
O  _parâmetro lpszProfileName_ será ignorado se houver uma sessão anterior chamada MapiLogonEx com o sinalizador MAPI_ALLOW_OTHERS definido e se o sinalizador MAPI_NEW_SESSION não estiver definido. Se o parâmetro  _lpszProfileName_ for NULL ou aponta para uma cadeia de caracteres vazia e o parâmetro  _flFlags_ incluir o sinalizador MAPI_LOGON_UI, a função MAPILogonEx gerará uma caixa de diálogo de logon com um campo vazio para o nome do perfil. 
  
Ao fazer logor em um perfil específico, um cliente deve passar o sinalizador MAPI_NEW_SESSION para MAPILogonEx, além do nome do perfil. Caso contrário, se outro cliente tiver estabelecido uma sessão compartilhada fazendo logon com o MAPI_ALLOW_OTHERS, o cliente será conectado à sessão compartilhada em vez de ao perfil solicitado. 
  
O MAPI_EXPLICIT_PROFILE sinalizador não faz com que o nome de perfil padrão seja usado quando  _lpszProfileName_ for NULL ou vazio, a menos que o sinalizador MAPI_USE_DEFAULT também esteja presente. 
  
O MAPI_NO_MAIL sinalizador tem vários efeitos que causam o seguinte ao não usar o spooler MAPI:
  
- Nenhuma mensagem pode ser enviada ou entregue pelo spooler MAPI durante esta sessão. Somente provedores de transporte e armazenamento fortemente próximos podem enviar e entregar mensagens. 
    
- Os armazenamentos baseados em servidor ainda podem enviar ou entregar mensagens. 
    
- As mensagens enviadas ou entregues por armazenamentos baseados em servidor não são processadas por provedores de ganchos. 
    
- Opções por mensagem e por destinatário para transporte não estão disponíveis. 
    
- A tabela de status não contém entradas para provedores de transporte, e nenhuma funcionalidade de transporte dependente de objetos de status (como configuração) está disponível. 
    
- A linha do spooler de mensagem na tabela de status contém o valor STATUS_FAILURE mensagem. 
    
- Logons sem retorno são permitidos, mas esses logons não fazem com que o logon anterior receba atualizações de objeto de status. 
    
Um serviço deve sempre fazer logoff usando o sinalizador MAPI_NO_MAIL linha. 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|MAPIObjects.cpp  <br/> |CMapiObjects::MAPILogonEx  <br/> |MFCMAPI usa o método MAPILogonEx para fazer logoff no MAPI.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md)
  
[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

