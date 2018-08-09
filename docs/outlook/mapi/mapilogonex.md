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
ms.openlocfilehash: 08782fe616fe260388cff8982dfbb09951453a00
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767985"
---
# <a name="mapilogonex"></a>MAPILogonEx

  
  
**Aplica-se a**: Outlook 
  
Logs de um aplicativo cliente em uma sessão com o sistema de mensagens. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapix.h  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Aplicativos cliente  <br/> |
   
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
  
> [in] Identificador para a janela para o qual a caixa de diálogo de logon é modal. Se nenhuma caixa de diálogo aparece durante a chamada, o parâmetro _ulUIParam_ será ignorado. Esse parâmetro pode ser zero. 
    
 _lpszProfileName_
  
> [in] Ponteiro para uma cadeia de caracteres que contém o nome do perfil para usar quando o usuário fizer logon. Esta cadeia de caracteres é limitada a 64 caracteres.
    
 _lpszPassword_
  
> [in] Ponteiro para uma cadeia de caracteres que contém a senha do perfil. O parâmetro _lpszPassword_ deve ser NULL. 
    
 _flFlags_
  
> [in] Bitmask dos sinalizadores usadas para controlar como o logon é executada. Sinalizadores a seguir podem ser definidos:
    
MAPI_ALLOW_OTHERS 
  
> A sessão compartilhada deve ser retornada, que permite que os clientes posteriores obtenham a sessão sem fornecer as credenciais de usuário. 
    
MAPI_BG_SESSION
  
> Fazer logon em uma sessão e executar todas as operações em segundo plano. Em geral, se um cliente pretende fazer processamento em um segmento de plano de fundo ou em um processo separado no modo não invasiva para o segmento de primeiro plano, ele deve chamar com o sinalizador MAPI_BG_SESSION. Um aplicativo cliente como um mecanismo de indexação ou abrir um arquivo de pastas particulares (PST) para acesso de tipo de plano de fundo são alguns exemplos de onde usar MAPI_BG_SESSION. MAPILogonEx.
    
MAPI_EXPLICIT_PROFILE 
  
> O perfil padrão não deve ser usado e o usuário deve ser solicitado a fornecer um perfil. 
    
MAPI_EXTENDED 
  
> Faça logon com recursos estendidos. Esse sinalizador deve sempre ser definido.
    
MAPI_FORCE_DOWNLOAD 
  
> Deve ser feita uma tentativa para baixar todas as mensagens do usuário antes de retornar. Se o sinalizador MAPI_FORCE_DOWNLOAD não estiver definido, as mensagens podem ser baixadas em segundo plano após a chamada para MAPILogonEx retorna. 
    
MAPI_LOGON_UI 
  
> Uma caixa de diálogo deve ser exibida para solicitar informações de logon do usuário, se necessário. Quando o sinalizador MAPI_LOGON_UI não estiver definido, o cliente da chamada não exibe uma caixa de diálogo de logon e retorna um valor de erro se o usuário não está conectado.
    
MAPI_NEW_SESSION 
  
> Deve ser feita uma tentativa para criar uma nova sessão MAPI, em vez de adquirir a sessão compartilhada. Se o sinalizador MAPI_NEW_SESSION não estiver definido, MAPILogonEx usa uma sessão compartilhada existente, mesmo se o parâmetro _lpszprofileName_ não for nulo. 
    
MAPI_NO_MAIL 
  
> MAPI não deve informar o spooler de MAPI de existência da sessão. O resultado é que nenhuma mensagem pode ser enviada ou recebida na sessão, exceto por meio de uma ligação estreita armazenar e par de transporte. Um cliente da chamada define esse sinalizador se ele está agindo como um operador, se o trabalho de configuração deve ser feito, ou se o cliente estiver navegando os repositórios de mensagem disponíveis. 
    
MAPI_NT_SERVICE 
  
> O chamador está sendo executado como um serviço do Windows. Chamadores que não estejam executando um serviço do Windows não deve definir esse sinalizador; os chamadores que estão sendo executados como um serviço devem definir esse sinalizador. 
    
MAPI_SERVICE_UI_ALWAYS 
  
> MAPILogonEx deve exibir uma caixa de diálogo de configuração para cada serviço de mensagem no perfil. As caixas de diálogo são exibidas depois que o perfil foi escolhido, mas antes de qualquer mensagem de serviço está conectado. A caixa de diálogo comuns de MAPI para logon também contém uma caixa de seleção que solicita a mesma operação. 
    
MAPI_TIMEOUT_SHORT 
  
> Fazer logon deve falhar se bloqueado por mais de alguns segundos. 
    
MAPI_UNICODE 
  
> As cadeias de caracteres passada na estão no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI. 
    
MAPI_USE_DEFAULT 
  
> O subsistema de mensagens deve substituir o nome do perfil do perfil padrão para o parâmetro _lpszProfileName_ . O sinalizador MAPI_EXPLICIT_PROFILE será ignorado, a menos que _lpszProfileName_ é nulo ou vazio. 
    
 _lppSession_
  
> [out] Ponteiro para um ponteiro para a interface de sessão MAPI.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> O logon bem-sucedido.
    
MAPI_E_LOGON_FAILED 
  
> O logon foi bem sucedido, porque um ou mais dos parâmetros para MAPILogonEx eram inválidos ou porque havia muitas sessões abertas já.
    
MAPI_E_TIMEOUT 
  
> MAPI serializa todos os logons por meio de um mutex. Isso será retornado se o sinalizador MAPI_TIMEOUT_SHORT foi definido e outro thread conduzidas a exclusão mútua. 
    
MAPI_E_USER_CANCEL 
  
> O usuário cancelou a operação, geralmente clicando no botão **Cancelar** em uma caixa de diálogo. 
    
## <a name="remarks"></a>Comentários

Aplicativos de cliente MAPI chamam a função de MAPILogonEx para fazer logon em uma sessão com o sistema de mensagens. Todas as cadeias de caracteres que são passadas e retornadas de e para chamadas MAPI são terminada em nulo e devem ser especificadas no conjunto de caracteres atual ou código de página do chamada cliente ou do provedor de sistema operacional.
  
O parâmetro _lpszProfileName_ é ignorado se não houver uma sessão anterior existente que chamado MapiLogonEx com o sinalizador MAPI_ALLOW_OTHERS definido e se o sinalizador MAPI_NEW_SESSION não estiver definida. Se o parâmetro _lpszProfileName_ é NULL ou aponta para uma sequência vazia e o parâmetro _flFlags_ inclui o sinalizador MAPI_LOGON_UI, a função MAPILogonEx gerará uma caixa de diálogo de logon que possui um campo vazio para o nome do perfil. 
  
Ao fazer logon em um perfil específico, um cliente deve passar o sinalizador MAPI_NEW_SESSION em MAPILogonEx além do nome de perfil. Caso contrário, se outro cliente tenha estabelecido uma sessão compartilhada fazendo logon com MAPI_ALLOW_OTHERS, o cliente será estar conectado à sessão compartilhada em vez de no perfil solicitada. 
  
O sinalizador MAPI_EXPLICIT_PROFILE não fará o nome de perfil padrão a ser usado ao _lpszProfileName_ é nulo ou vazio, a menos que o sinalizador MAPI_USE_DEFAULT também está presente. 
  
O sinalizador MAPI_NO_MAIL tem vários efeitos que causam o seguinte quando não usando o MAPI spooler:
  
- Nenhuma mensagem pode ser enviada ou entregue pelo spooler MAPI durante a sessão. Únicos provedores de armazenamento e transporte de ligação estreita podem enviar e entregar mensagens. 
    
- Repositórios de baseado em servidor ainda podem enviar ou entregar mensagens. 
    
- Mensagens enviadas ou viabilizadas pela repositórios com base em servidor não são processadas por quaisquer provedores de fora do gancho. 
    
- Opções-message e por destinatário para transportes não estão disponíveis. 
    
- A tabela de status não contiver entradas para provedores de transporte e qualquer funcionalidade de transporte dependentes de objetos de status (por exemplo, a configuração) não está disponível. 
    
- Linha da tabela de status spooler mensagem contém o valor STATUS_FAILURE. 
    
- Logons acumuladas são permitidas, mas os logons não farão com que o logon anterior receber atualizações de status de objeto. 
    
Um serviço sempre deve fazer logon usando o sinalizador MAPI_NO_MAIL. 
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|MAPIObjects.cpp  <br/> |CMapiObjects::MAPILogonEx  <br/> |MFCMAPI usa o método MAPILogonEx para fazer logon no MAPI.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md)
  
[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)

