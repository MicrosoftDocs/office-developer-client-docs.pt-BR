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
ms.openlocfilehash: a599a6fe5093e52e50d33a1761df5689b7335138
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568291"
---
# <a name="imsgserviceadminconfiguremsgservice"></a>IMsgServiceAdmin::ConfigureMsgService

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Reconfigura um serviço de mensagem.
  
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
  
> [in] Um ponteiro para a estrutura [MAPIUID](mapiuid.md) que contém o identificador exclusivo para o serviço de mensagem configurar. 
    
 _ulUIParam_
  
> [in] Uma alça para a janela pai da folha de propriedades de configuração.
    
 _ulFlags_
  
> [in] Uma bitmask dos sinalizadores que controla a exibição da folha de propriedades. Sinalizadores a seguir podem ser definidos:
    
MAPI_UNICODE 
  
> As cadeias de caracteres passada na estão no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI.
    
MSG_SERVICE_UI_READ_ONLY 
  
> O serviço de mensagem deve exibir sua folha de propriedades de configuração, mas não permitir que o usuário alterá-la. A maioria dos serviços de mensagem ignorar esse sinalizador.
    
SERVICE_UI_ALLOWED 
  
> O serviço de mensagem deve exibir sua folha de propriedades de configuração somente se o serviço não estiver completamente configurado.
    
SERVICE_UI_ALWAYS 
  
> O serviço de mensagem deve sempre exibir sua folha de propriedades de configuração. Se SERVICE_UI_ALWAYS não estiver definida, uma folha de propriedades de configuração ainda pode ser exibida se SERVICE_UI_ALLOWED for definido e informações de configuração válida não estão disponíveis na matriz de valores de propriedade no parâmetro _lpProps_ . SERVICE_UI_ALLOWED ou SERVICE_UI_ALWAYS deve ser definida para uma folha de propriedades a ser exibido. 
    
 _cValues_
  
> [in] A contagem de valores de propriedade na estrutura [SPropValue](spropvalue.md) apontado pela _lpProps_. 
    
 _lpProps_
  
> [in] Um ponteiro para uma matriz de valores de propriedade que descrevem as propriedades a serem exibidas na folha de propriedades. O parâmetro _lpProps_ não deve ser NULL se o serviço de mensagem deve ser configurado sem uma interface do usuário. 
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> O serviço de mensagem foi configurado com êxito.
    
MAPI_E_EXTENDED_ERROR 
  
> Um erro específico para um serviço de mensagem. Para obter a estrutura [MAPIERROR](mapierror.md) que descreve o erro, o aplicativo cliente deve chamar o método [IMsgServiceAdmin::GetLastError](imsgserviceadmin-getlasterror.md) . 
    
E_NOT_FOUND 
  
> **MAPIUID** apontado pela _lpUID_ não corresponde àquele de um serviço de mensagem existente. 
    
MAPI_E_NOT_INITIALIZED 
  
> O serviço de mensagem não tem uma entrada aponte a função.
    
MAPI_E_USER_CANCEL 
  
> O usuário cancelou a operação, geralmente clicando no botão **Cancelar** na folha de propriedades. 
    
## <a name="remarks"></a>Comentários

O método **IMsgServiceAdmin::ConfigureMsgService** permite que um serviço de mensagem a ser configurado, com ou sem uma folha de propriedades de configuração. 
  
Para permitir que a configuração sem uma exibição de folha de propriedade, serviços de mensagem normalmente preparam um arquivo de cabeçalho que inclui as constantes para todas as propriedades obrigatórios e opcionais e seus valores.
  
## <a name="notes-to-callers"></a>Notas para chamadores

Para recuperar a estrutura **MAPIUID** para configurar o serviço de mensagem, recupere a coluna **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) da linha do serviço de mensagem da tabela de serviço de mensagem. Para obter mais informações, consulte o procedimento descrito no método [IMsgServiceAdmin:: CreateMsgService](imsgserviceadmin-createmsgservice.md) . 
  
Você pode configurar um serviço de mensagem sem exibir uma folha de propriedades para um usuário somente se você tiver o avanço informações sobre os valores de propriedade a ser definido. Se você estiver configurando um serviço de mensagem sem exibir uma folha de propriedades, passar valores de propriedade válido no parâmetro _lpProps_ e não definir os sinalizadores MSG_SERVICE_UI_READ_ONLY, SERVICE_UI_ALLOWED ou SERVICE_UI_ALWAYS. 
  
Se você receber todas ou algumas das informações de configuração do usuário por meio de uma folha de propriedades, defina SERVICE_UI_ALLOWED em _ulFlags_. Se você usar as informações existentes da propriedade apenas para estabelecer as configurações padrão e o usuário é capaz de alterar as configurações, defina SERVICE_UI_ALWAYS em _ulFlags_.
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|MAPIProfileFunctions.cpp  <br/> |HrAddServiceToProfile  <br/> |MFCMAPI usa o método **IMsgServiceAdmin::ConfigureMsgService** para configurar um serviço que tenha sido adicionado a um perfil.  <br/> |
   
## <a name="see-also"></a>Confira também



[MAPIUID](mapiuid.md)
  
[SPropValue](spropvalue.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)

