---
title: IMsgServiceAdminCreateMsgService
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.CreateMsgService
api_type:
- COM
ms.assetid: 0135f049-0311-45e5-9685-78597d599a4e
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: e7d30c1aba8ddc1419045c1caa8524f7d2063dc5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317387"
---
# <a name="imsgserviceadmincreatemsgservice"></a>IMsgServiceAdmin::CreateMsgService

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
PreTerido: o uso de [IMsgServiceAdmin2:: CreateMsgServiceEx](imsgserviceadmin2-createmsgserviceex.md) é recomendado. Adiciona um serviço de mensagens ao perfil atual. 
  
```cpp
HRESULT CreateMsgService(
  LPSTR lpszService,
  LPSTR lpszDisplayName,
  ULONG_PTR ulUIParam,
  ULONG ulFlags    
);
```

## <a name="parameters"></a>Parâmetros

 _lpszService_
  
> no Um ponteiro para o nome do serviço de mensagens a ser adicionado. Esse nome de serviço de mensagem deve aparecer na seção **[serviços]** do arquivo MapiSvc. inf. 
    
 _lpszDisplayName_
  
> no Um ponteiro para o nome de exibição do serviço de mensagens a ser adicionado. O parâmetro _lpszDisplayName_ será ignorado se o serviço de mensagens tiver definido a propriedade **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) no arquivo MapiSvc. inf.
    
 _ulUIParam_
  
> no Uma alça para a janela pai de qualquer caixa de diálogo ou Windows este método é exibido.
    
 _ulFlags_
  
> no Uma bitmask de sinalizadores que controla como o serviço de mensagens é instalado. Os seguintes sinalizadores podem ser definidos:
    
MAPI_UNICODE
  
> Os parâmetros lpszService e lpszDisplayName devem ser convertidos em LPWSTR e interpretados como cadeias de caracteres Unicode.
    
SERVICE_NO_RESTART_WARNING
  
> Ao adicionar um novo serviço de mensagens ao perfil, o subsistema MAPI, com base em várias circunstâncias e critérios, geralmente determina que essa ação requer uma reinicialização do Outlook. Se o sinalizador SERVICE_NO_RESTART_WARNING não estiver incluído e a interface do usuário for baseada nos sinalizadores SERVICE_UI_ALWAYS e SERVICE_UI_ALLOWED e pelo menos um processo estiver conectado ao perfil atual, essa função exibirá a mensagem "você deve reiniciar o Outlook para que as alterações entrem em vigor. " Incluir o sinalizador SERVICE_NO_RESTART_WARNING suprime a exibição dessa mensagem de aviso.
    
SERVICE_UI_ALLOWED
  
> A interface do usuário de configuração do serviço de mensagens é permitida se necessário.
    
SERVICE_UI_ALWAYS 
  
> O serviço de mensagens exibe sua folha de propriedades de configuração.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada teve êxito e retornou o valor ou valores esperados.
    
MAPI_E_NOT_FOUND 
  
> O nome do serviço de mensagens não está na seção **[serviços]** de MapiSvc. inf. 
    
## <a name="remarks"></a>Comentários

O método **IMsgServiceAdmin:: CreateMsgService** adiciona um serviço de mensagens ao perfil atual. **CreateMsgService** chama a função de ponto de entrada do serviço de mensagens para executar qualquer tarefa de configuração específica do serviço. Se o sinalizador SERVICE_UI_ALLOWED estiver definido no parâmetro _parâmetroulflags_ , o serviço de mensagens que estiver sendo instalado poderá exibir uma folha de propriedades para permitir que o usuário defina suas configurações. 
  
O arquivo MapiSvc. inf contém a lista de provedores que compõem um serviço de mensagens e as propriedades de cada um. **CreateMsgService** primeiro cria uma nova seção de perfil para o serviço de mensagens e, em seguida, copia Todas as informações desse serviço do arquivo MapiSvc. inf para o perfil, criando novas seções para cada provedor. 
  
Após todas as informações terem sido copiadas de MapiSvc. inf, a função de ponto de entrada do serviço de mensagens é chamada com o valor MSG_SERVICE_CREATE definido no parâmetro _ulContext_ . Se o sinalizador SERVICE_UI_ALLOWED estiver definido no parâmetro _parâmetroulflags_ do método **CreateMsgService** , os valores nos parâmetros _ulUIParam_ e _parâmetroulflags_ também serão passados quando a função de ponto de entrada do serviço de mensagens for chamada. Os provedores de serviços devem exibir suas folhas de propriedades de configuração para que os usuários possam configurar o serviço de mensagens. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

 **CreateMsgService** não retorna a estrutura [MAPIUID](mapiuid.md) para o serviço de mensagem que foi adicionado ao perfil. 
  
Para recuperar o **MAPIUID** do serviço de mensagens criadas, use o seguinte procedimento: 
  
1. Chame o método [IMsgServiceAdmin:: GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) para obter a tabela de administração do serviço de mensagens. 
    
2. Localize a linha que representa o serviço de mensagem, colocando uma restrição na tabela que corresponde à propriedade **PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md)) com o nome do serviço de mensagens. 
    
3. Recupere a propriedade **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) do serviço. 
    
4. Passe o valor da propriedade **PR_SERVICE_UID** no parâmetro _lpUid_ para o método [IMsgServiceAdmin:: ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) para configurar o serviço. 
    
> [!CAUTION]
> A implementação do Microsoft Outlook 2010 do subsistema MAPI não oferece suporte ao MAPI_UNICODE e falhará se for usado. 
  
> [!IMPORTANT]
> O _parâmetroulflags_ SERVICE_NO_RESTART_WARNING pode não estar definido no arquivo de cabeçalho baixável que você tem atualmente, e, nesse caso, você pode adicioná-lo ao seu código usando o seguinte valor: >`#define SERVICE_NO_RESTART_WARNING 0x00000080`
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|MAPIProfileFunctions. cpp  <br/> |HrAddServiceToProfile  <br/> |MFCMAPI usa o método **IMsgServiceAdmin:: CreateMsgService** para adicionar um serviço a um perfil.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

