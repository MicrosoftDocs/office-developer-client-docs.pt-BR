---
title: IMsgServiceAdminConfigureMsgService
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.ConfigureMsgService
api_type:
- COM
ms.assetid: a08f5905-2585-49ca-abb7-a77f2736f604
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 87ac394f9ab77b092cdfcd44f65b040a039319e7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422184"
---
# <a name="imsgserviceadminconfiguremsgservice"></a>IMsgServiceAdmin::ConfigureMsgService

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Reconfigura um serviço de mensagens.
  
```cpp
HRESULT ConfigureMsgService(
  LPMAPIUID lpUID,
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  ULONG cValues,
  LPSPropValue lpProps
);
```

## <a name="parameters"></a>Parâmetros

 _lpUID_
  
> [in] Um ponteiro para a [estrutura MAPIUID](mapiuid.md) que contém o identificador exclusivo para o serviço de mensagens configurar. 
    
 _ulUIParam_
  
> [in] Um alça para a janela pai da folha de propriedades de configuração.
    
 _ulFlags_
  
> [in] Uma máscara de bits de sinalizadores que controla a exibição da folha de propriedades. Os sinalizadores a seguir podem ser definidos:
    
MAPI_UNICODE 
  
> As cadeias de caracteres passadas estão no formato Unicode. Se o MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI.
    
MSG_SERVICE_UI_READ_ONLY 
  
> O serviço de mensagens deve exibir sua folha de propriedades de configuração, mas não permitir que o usuário a altere. A maioria dos serviços de mensagens ignora esse sinalizador.
    
SERVICE_UI_ALLOWED 
  
> O serviço de mensagens deve exibir sua folha de propriedades de configuração somente se o serviço não estiver completamente configurado.
    
SERVICE_UI_ALWAYS 
  
> O serviço de mensagens deve sempre exibir sua folha de propriedades de configuração. Se SERVICE_UI_ALWAYS não estiver definida, uma folha de propriedades de configuração ainda poderá ser exibida se SERVICE_UI_ALLOWED estiver definida e as informações de configuração válidas não estarão disponíveis na matriz de valores de propriedade no parâmetro _lpProps._ As SERVICE_UI_ALLOWED ou SERVICE_UI_ALWAYS devem ser definidas para que uma folha de propriedades seja exibida. 
    
 _cValues_
  
> [in] A contagem de valores de propriedade [na estrutura SPropValue](spropvalue.md) apontado por  _lpProps_. 
    
 _lpProps_
  
> [in] Um ponteiro para uma matriz de valores de propriedade que descrevem as propriedades a exibir na folha de propriedades. O  _parâmetro lpProps_ não deve ser NULL se o serviço de mensagens deve ser configurado sem uma interface do usuário. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O serviço de mensagens foi configurado com êxito.
    
MAPI_E_EXTENDED_ERROR 
  
> Um erro específico de um serviço de mensagens. Para obter a [estrutura MAPIERROR](mapierror.md) que descreve o erro, o aplicativo cliente deve chamar o método [IMsgServiceAdmin::GetLastError.](imsgserviceadmin-getlasterror.md) 
    
MAPI_E_NOT_FOUND 
  
> O **MAPIUID** apontado por  _lpUID_ não é igual ao de um serviço de mensagens existente. 
    
MAPI_E_NOT_INITIALIZED 
  
> O serviço de mensagens não tem uma função de ponto de entrada.
    
MAPI_E_USER_CANCEL 
  
> O usuário cancelou a operação, normalmente clicando no botão **Cancelar** na folha de propriedades. 
    
## <a name="remarks"></a>Comentários

O **método IMsgServiceAdmin::ConfigureMsgService** permite que um serviço de mensagens seja configurado, com ou sem uma folha de propriedades de configuração. 
  
Para permitir a configuração sem uma exibição de folha de propriedades, os serviços de mensagens normalmente preparam um arquivo de header que inclui constantes para todas as propriedades necessárias e opcionais e seus valores.
  
## <a name="notes-to-callers"></a>Notas para chamadores

Para recuperar a estrutura **MAPIUID** do serviço de mensagens a ser configurada, recupere a coluna **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) da linha do serviço de mensagens na tabela de serviço de mensagens. Para obter mais informações, consulte o procedimento descrito no [método IMsgServiceAdmin::CreateMsgService.](imsgserviceadmin-createmsgservice.md) 
  
Você pode configurar um serviço de mensagens sem exibir uma folha de propriedades para um usuário somente se tiver informações antecipadas sobre os valores de propriedade a serem definidos. Se você estiver configurando um serviço de mensagem sem exibir uma folha de propriedades, passe valores de propriedade válidos no parâmetro  _lpProps_ e não de definir os sinalizadores MSG_SERVICE_UI_READ_ONLY, SERVICE_UI_ALLOWED ou SERVICE_UI_ALWAYS. 
  
Se você receber todas ou algumas das informações de configuração do usuário por meio de uma folha de propriedades, defina SERVICE_UI_ALLOWED em  _ulFlags_. Se você usar informações de propriedade existentes apenas para estabelecer configurações padrão e o usuário for capaz de alterar as configurações, defina SERVICE_UI_ALWAYS  _em ulFlags_.
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|MAPIProfileFunctions.cpp  <br/> |HrAddServiceToProfile  <br/> |MFCMAPI usa o **método IMsgServiceAdmin::ConfigureMsgService** para configurar um serviço que foi adicionado a um perfil.  <br/> |
   
## <a name="see-also"></a>Confira também



[MAPIUID](mapiuid.md)
  
[SPropValue](spropvalue.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

