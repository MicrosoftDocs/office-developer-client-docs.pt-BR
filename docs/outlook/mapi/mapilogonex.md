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
|Arquivo de cabeçalho:  <br/> |Mapix. h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos cliente  <br/> |
   
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
  
> no Manipulador para a janela à qual a caixa de diálogo de logon é modal. Se nenhuma caixa de diálogo for exibida durante a chamada, o parâmetro _ulUIParam_ será ignorado. Esse parâmetro pode ser zero. 
    
 _lpszProfileName_
  
> no Ponteiro para uma cadeia de caracteres que contém o nome do perfil a ser usado quando o usuário faz logon. Esta cadeia de caracteres é limitada a 64 caracteres.
    
 _lpszPassword_
  
> no Ponteiro para uma cadeia de caracteres que contém a senha do perfil. O parâmetro _lpszPassword_ deve ser nulo. 
    
 _Parâmetroflflags_
  
> no Bitmask dos sinalizadores usados para controlar como o logon é executado. Os seguintes sinalizadores podem ser definidos:
    
MAPI_ALLOW_OTHERS 
  
> A sessão compartilhada deve ser retornada, permitindo que os clientes posteriores obtenham a sessão sem fornecer nenhuma credencial de usuário. 
    
MAPI_BG_SESSION
  
> Faça logon em uma sessão e execute qualquer operação em segundo plano. Em geral, se um cliente pretende fazer o processamento em um thread de segundo plano ou em um processo separado de uma maneira que não é invasiva para o thread de primeiro plano, ele deve chamar com o sinalizador MAPI_BG_SESSION. Um aplicativo cliente, como um mecanismo de indexação ou a abertura de um arquivo de pastas particulares (PST) para acesso de tipo de plano de fundo, são alguns exemplos de onde usar o MAPI_BG_SESSION. Funçãomapilogonex.
    
MAPI_EXPLICIT_PROFILE 
  
> O perfil padrão não deve ser usado e o usuário deve ser solicitado a fornecer um perfil. 
    
MAPI_EXTENDED 
  
> Faça logon com recursos estendidos. Esse sinalizador deve sempre ser definido.
    
MAPI_FORCE_DOWNLOAD 
  
> Uma tentativa deve ser feita para baixar todas as mensagens do usuário antes de retornar. Se o sinalizador MAPI_FORCE_DOWNLOAD não estiver definido, as mensagens poderão ser baixadas em segundo plano depois que a chamada para Funçãomapilogonex retornar. 
    
MAPI_LOGON_UI 
  
> Uma caixa de diálogo deve ser exibida para solicitar ao usuário as informações de logon, se necessário. Quando o sinalizador MAPI_LOGON_UI não estiver definido, o cliente de chamada não exibirá uma caixa de diálogo de logon e retornará um valor de erro se o usuário não estiver conectado.
    
MAPI_NEW_SESSION 
  
> Uma tentativa deve ser feita para criar uma nova sessão MAPI em vez de adquirir a sessão compartilhada. Se o sinalizador MAPI_NEW_SESSION não estiver definido, o Funçãomapilogonex usará uma sessão compartilhada existente, mesmo que o parâmetro _lpszprofileName_ não seja nulo. 
    
MAPI_NO_MAIL 
  
> O MAPI não deve informar o spooler MAPI da existência da sessão. O resultado é que nenhuma mensagem pode ser enviada ou recebida na sessão, exceto por meio de um par de transporte e transporte rigidamente acoplado. Um cliente de chamada define esse sinalizador se ele estiver atuando como um agente, se o trabalho de configuração tiver de ser feito ou se o cliente estiver pesquisando os repositórios de mensagens disponíveis. 
    
MAPI_NT_SERVICE 
  
> O chamador está sendo executado como um serviço do Windows. Os chamadores que não estão sendo executados como um serviço do Windows não devem definir esse sinalizador; os chamadores que estão executando como um serviço devem definir esse sinalizador. 
    
MAPI_SERVICE_UI_ALWAYS 
  
> Funçãomapilogonex deve exibir uma caixa de diálogo de configuração para cada serviço de mensagens no perfil. As caixas de diálogo são exibidas após o perfil ter sido escolhido, mas antes de qualquer serviço de mensagem estar conectado. A caixa de diálogo comum de MAPI para logon também contém uma caixa de seleção que solicita a mesma operação. 
    
MAPI_TIMEOUT_SHORT 
  
> O logon deve falhar se bloqueado por mais de alguns segundos. 
    
MAPI_UNICODE 
  
> As cadeias de caracteres passadas estão no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estarão no formato ANSI. 
    
MAPI_USE_DEFAULT 
  
> O subsistema de mensagens deve substituir o nome do perfil do perfil padrão para o parâmetro _lpszProfileName_ . O sinalizador MAPI_EXPLICIT_PROFILE é ignorado, a menos que _lpszProfileName_ seja nulo ou vazio. 
    
 _lppSession_
  
> bota Ponteiro para um ponteiro para a interface de sessão MAPI.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O logon foi bem-sucedido.
    
MAPI_E_LOGON_FAILED 
  
> O logon não foi bem-sucedido, porque um ou mais parâmetros para Funçãomapilogonex eram inválidos ou porque já havia muitas sessões abertas.
    
MAPI_E_TIMEOUT 
  
> O MAPI serializa todos os logons por meio de um mutex. Isso será retornado se o sinalizador MAPI_TIMEOUT_SHORT tiver sido definido e outro thread tiver mantido o mutex. 
    
MAPI_E_USER_CANCEL 
  
> O usuário cancelou a operação, geralmente clicando no botão **Cancelar** em uma caixa de diálogo. 
    
## <a name="remarks"></a>Comentários

Os aplicativos cliente MAPI chamam a função Funçãomapilogonex para fazer logon em uma sessão com o sistema de mensagens. Todas as cadeias de caracteres que são passadas e retornadas para e de chamadas MAPI são terminadas em nulo e devem ser especificadas no conjunto de caracteres atual ou na página de códigos do sistema operacional do cliente ou provedor de chamadas.
  
O parâmetro _lpszProfileName_ será ignorado se houver uma sessão anterior existente que chamou funçãomapilogonex com o sinalizador MAPI_ALLOW_OTHERS definido e se o sinalizador MAPI_NEW_SESSION não estiver definido. Se o parâmetro _lpszProfileName_ for NULL ou apontar para uma cadeia de caracteres vazia, e o parâmetro _parâmetroflflags_ incluir o sinalizador MAPI_LOGON_UI, a função funçãomapilogonex gerará uma caixa de diálogo de logon que tem um campo vazio para o nome do perfil. 
  
Ao fazer logon em um perfil específico, um cliente deve passar o sinalizador MAPI_NEW_SESSION para o Funçãomapilogonex, além do nome do perfil. Caso contrário, se outro cliente tiver estabelecido uma sessão compartilhada fazendo logon com o MAPI_ALLOW_OTHERS, o cliente será conectado à sessão compartilhada em vez de ao perfil solicitado. 
  
O sinalizador MAPI_EXPLICIT_PROFILE não faz com que o nome do perfil padrão seja usado quando _lpszProfileName_ é nulo ou vazio, a menos que o sinalizador MAPI_USE_DEFAULT também esteja presente. 
  
O sinalizador MAPI_NO_MAIL tem vários efeitos que causam o seguinte quando não usam o MAPI spooler:
  
- Nenhuma mensagem pode ser enviada ou entregue pelo spooler MAPI durante esta sessão. Somente provedores de armazenamento e transporte rigidamente acoplados podem enviar e entregar mensagens. 
    
- Os repositórios baseados em servidor ainda podem enviar ou entregar mensagens. 
    
- As mensagens enviadas ou entregues por repositórios baseados em servidor não são processadas por provedores de conexão. 
    
- As opções por mensagem e por destinatário para transportes não estão disponíveis. 
    
- A tabela de status não contém entradas para provedores de transporte e qualquer funcionalidade de transporte dependente de objetos de status (como configuração) não está disponível. 
    
- A linha de spooler de mensagem na tabela status contém o valor STATUS_FAILURE. 
    
- Os logons acumulados são permitidos, mas esses logons não fazem o logon anterior receber atualizações de objetos de status. 
    
Um serviço deve sempre fazer logon usando o sinalizador MAPI_NO_MAIL. 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|MAPIObjects. cpp  <br/> |CMapiObjects:: Funçãomapilogonex  <br/> |MFCMAPI usa o método Funçãomapilogonex para fazer logon no MAPI.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md)
  
[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

