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
ms.openlocfilehash: 7c649680d1d04e210ac4d90779e9a4e57aaab25a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579862"
---
# <a name="imsgserviceadmincreatemsgservice"></a>IMsgServiceAdmin::CreateMsgService

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Preterido: O uso de [IMsgServiceAdmin2::CreateMsgServiceEx](imsgserviceadmin2-createmsgserviceex.md) é recomendável. Adiciona um serviço de mensagem ao perfil atual. 
  
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
  
> [in] Um ponteiro para o nome do serviço de mensagem para adicionar. Esse nome de serviço de mensagem deve aparecer na seção **[Services]** do arquivo Mapisvc. 
    
 _lpszDisplayName_
  
> [in] Um ponteiro para o nome de exibição do serviço de mensagem para adicionar. O parâmetro _lpszDisplayName_ será ignorado se o serviço de mensagem definiu a propriedade **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) no arquivo Mapisvc.
    
 _ulUIParam_
  
> [in] Um identificador para a janela do pai de quaisquer caixas de diálogo ou windows esse método exibe.
    
 _ulFlags_
  
> [in] Uma bitmask dos sinalizadores que controla como o serviço de mensagem está instalado. Sinalizadores a seguir podem ser definidos:
    
MAPI_UNICODE
  
> Parâmetros lpszDisplayName e o lpszService devem ser convertidos em LPWSTR e interpretados como cadeias de caracteres Unicode.
    
SERVICE_NO_RESTART_WARNING
  
> Ao adicionar um novo serviço de mensagem ao perfil, o subsistema MAPI, com base em várias circunstâncias e critérios, geralmente determina que esta ação exige uma reinicialização do Outlook. Se o sinalizador SERVICE_NO_RESTART_WARNING não está incluído e interface do usuário é permitida - com base nos sinalizadores SERVICE_UI_ALWAYS e SERVICE_UI_ALLOWED - e pelo menos um processo é feito logon no perfil atual, essa função exibe a mensagem "você deve reiniciar o Outlook para Essas alterações entrem em vigor." Incluindo o sinalizador SERVICE_NO_RESTART_WARNING suprime a exibição dessa mensagem de aviso.
    
SERVICE_UI_ALLOWED
  
> A configuração do serviço de mensagem permitido UI se necessário.
    
SERVICE_UI_ALWAYS 
  
> O serviço de mensagem exibe sua folha de propriedades de configuração.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores.
    
E_NOT_FOUND 
  
> O nome do serviço de mensagem não está na seção **[Services]** da Mapisvc. 
    
## <a name="remarks"></a>Comentários

O método **IMsgServiceAdmin:: CreateMsgService** adiciona um serviço de mensagem ao perfil atual. **CreateMsgService** chama a função de ponto de entrada do serviço de mensagem para executar tarefas específicas do serviço de configuração. Se o sinalizador SERVICE_UI_ALLOWED é definido no parâmetro _ulFlags_ , o serviço de mensagem que está sendo instalado pode exibir uma folha de propriedades para permitir que o usuário definir suas configurações. 
  
O arquivo Mapisvc contém uma lista de provedores que compõem um serviço de mensagem e as propriedades para cada um. **CreateMsgService** primeiro cria uma nova seção de perfil para o serviço de mensagem e, em seguida, copia todas as informações para o serviço do arquivo Mapisvc exe para o perfil, criando novas seções para cada provedor. 
  
Depois que todas as informações foram copiadas dos Mapisvc, função do ponto de entrada do serviço de mensagem é chamada com o valor MSG_SERVICE_CREATE definido no parâmetro _ulContext_ . Se o sinalizador SERVICE_UI_ALLOWED é definido no parâmetro de _ulFlags_ do método **CreateMsgService** , os valores nos parâmetros _ulUIParam_ e _ulFlags_ também são passados quando a função de ponto de entrada do serviço de mensagem é chamada. Provedores de serviços devem exibir suas folhas de propriedades de configuração para que os usuários podem configurar o serviço de mensagem. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

 **CreateMsgService** não retorna a estrutura [MAPIUID](mapiuid.md) para o serviço de mensagem que foi adicionada ao perfil. 
  
Para recuperar o **MAPIUID** para o serviço de mensagem criada, use o procedimento a seguir: 
  
1. Chame o método [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) para obter a tabela de administração de serviços de mensagem. 
    
2. Localize a linha que representa o serviço de mensagem, colocando uma restrição na tabela que corresponda a propriedade **PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md)) com o nome do serviço de mensagem. 
    
3. Recupere a propriedade do serviço **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)). 
    
4. Passe o valor da propriedade **PR_SERVICE_UID** no parâmetro _lpUid_ para o método [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) para configurar o serviço. 
    
> [!CAUTION]
> A implementação do Microsoft Outlook 2010 do subsistema de MAPI não suporta MAPI_UNICODE e irá falhar se for usado. 
  
> [!IMPORTANT]
> _UlFlags_ SERVICE_NO_RESTART_WARNING não podem ser definidos no arquivo de cabeçalho para download que você possui atualmente, nesse caso, você pode adicioná-lo para seu código usando o seguinte valor: >`#define SERVICE_NO_RESTART_WARNING 0x00000080`
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|MAPIProfileFunctions.cpp  <br/> |HrAddServiceToProfile  <br/> |MFCMAPI usa o método **IMsgServiceAdmin:: CreateMsgService** para adicionar um serviço a um perfil.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)

