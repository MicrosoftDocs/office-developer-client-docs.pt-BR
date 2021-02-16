---
title: IProfAdminCreateProfile
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.CreateProfile
api_type:
- COM
ms.assetid: 10cda14a-8f93-41e0-b1fb-500098bdc392
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: b104c62eb617e6c68f85dea4ef6379c831733844
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404397"
---
# <a name="iprofadmincreateprofile"></a>IProfAdmin::CreateProfile

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Cria um novo perfil.
  
```cpp
HRESULT CreateProfile(
  LPSTR lpszProfileName,
  LPSTR lpszPassword,
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parâmetros

 _lpszProfileName_
  
> [in] Um ponteiro para o nome do novo perfil.
    
 _lpszPassword_
  
> [in] Um ponteiro para a senha do novo perfil. 
    
 _ulUIParam_
  
> [in] Um alça para a janela pai de quaisquer caixas de diálogo ou janelas que esse método exibe.
    
 _ulFlags_
  
> [in] Uma máscara de bits de sinalizadores que controla como o perfil é criado. Os sinalizadores a seguir podem ser definidos:
    
MAPI_DEFAULT_SERVICES 
  
> MAPI should populate the new profile with the message services that are included in the [Default Services] section of the Mapisvc.inf file.
    
MAPI_DIALOG 
  
> As folhas de propriedades de configuração de cada um dos provedores nos serviços de mensagem a serem adicionados podem ser exibidas. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O novo perfil foi criado.
    
MAPI_E_NO_ACCESS 
  
> O novo perfil especificado já existe.
    
## <a name="remarks"></a>Comentários

O **método IProfAdmin::CreateProfile** cria um novo perfil. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Você pode chamar **CreateProfile no** momento da instalação do aplicativo ou a qualquer momento durante uma sessão. Quando esse método é chamado no momento da instalação, muitas das definições de configuração vêm do arquivo de configuração Mapisvc.inf. Quando esse método é chamado durante uma sessão ativa, as configurações vêm do usuário que é solicitado por meio de uma série de folhas de propriedades. 
  
Se o sinalizador MAPI_DEFAULT_SERVICES for definido no parâmetro  _ulFlags,_ **CreateProfile** chamará a função de ponto de entrada do serviço de mensagens para cada serviço de mensagem na seção [Serviços Padrão] no arquivo Mapisvc.inf. Cada função de ponto de entrada do serviço de mensagens é chamada com o  _parâmetro ulContext_ definido como MSG_SERVICE_CREATE. 
  
Se os sinalizadores MAPI_DIALOG e MAPI_DEFAULT_SERVICES da mensagem estão definidos, os valores nos parâmetros  _ulUIParam_ e  _ulFlags_ também são passados para a função de ponto de entrada do serviço de mensagens. As funções de ponto de entrada do serviço de mensagens são chamadas somente depois que todas as informações disponíveis do arquivo Mapisvc.inf foram adicionadas ao perfil. 
  
O nome do novo perfil e sua senha podem ter até 64 caracteres e podem incluir os seguintes caracteres:
  
- Todos os caracteres alfanuméricos, incluindo caracteres de ênfase e o caractere de sublinhado.
    
- Espaços incorporados, mas não espaços à frente ou à frente.
    
O  _parâmetro lpszPassword_ deve ser NULL ou um ponteiro para uma cadeia de caracteres de comprimento zero. 
  
## <a name="see-also"></a>Confira também



[IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)
  
[IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md)
  
[MSGSERVICEENTRY](msgserviceentry.md)
  
[IProfAdmin : IUnknown](iprofadminiunknown.md)

