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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317112"
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
  
> no Um ponteiro para o nome do novo perfil.
    
 _lpszPassword_
  
> no Um ponteiro para a senha do novo perfil. 
    
 _ulUIParam_
  
> no Uma alça para a janela pai de quaisquer caixas de diálogo ou janelas que esse método exibe.
    
 _ulFlags_
  
> no Uma bitmask de sinalizadores que controla como o perfil é criado. Os seguintes sinalizadores podem ser definidos:
    
MAPI_DEFAULT_SERVICES 
  
> O MAPI deve preencher o novo perfil com os serviços de mensagem incluídos na seção [serviços padrão] do arquivo MAPISVC. inf.
    
MAPI_DIALOG 
  
> É possível exibir as folhas de propriedades de configuração de cada um dos provedores nos serviços de mensagens a serem adicionados. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O novo perfil foi criado.
    
MAPI_E_NO_ACCESS 
  
> O novo perfil especificado já existe.
    
## <a name="remarks"></a>Comentários

O método **IProfAdmin:: CreateProfile** cria um novo perfil. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Você pode chamar **CreateProfile** no momento da instalação do aplicativo ou a qualquer momento durante uma sessão. Quando esse método é chamado no momento da instalação, muitas das definições de configuração são provenientes do arquivo de configuração MAPISVC. inf. Quando esse método é chamado durante uma sessão ativa, as configurações são provenientes do usuário que é solicitado através de uma série de folhas de propriedades. 
  
Se o sinalizador MAPI_DEFAULT_SERVICES estiver definido no parâmetro _parâmetroulflags_ , **CreateProfile** chamará a função de ponto de entrada do serviço de mensagens para cada serviço de mensagens na seção [serviços padrão] no arquivo MAPISVC. inf. Cada função de ponto de entrada de serviço de mensagens é chamada com o parâmetro _ulContext_ definido como MSG_SERVICE_CREATE. 
  
Se ambos os sinalizadores MAPI_DIALOG e MAPI_DEFAULT_SERVICES estiverem definidos, os valores nos parâmetros _ulUIParam_ e _parâmetroulflags_ também serão passados para a função de ponto de entrada de serviço de mensagens. As funções do ponto de entrada do serviço de mensagens são chamadas somente depois que todas as informações disponíveis do arquivo MAPISVC. inf forem adicionadas ao perfil. 
  
O nome do novo perfil e sua senha podem ter até 64 caracteres de comprimento e podem incluir os seguintes caracteres:
  
- Todos os caracteres alfanuméricos, incluindo caracteres de ênfase e o caractere de sublinhado.
    
- Espaços incorporados, mas não espaços à esquerda ou à direita.
    
O parâmetro _lpszPassword_ deve ser NULL ou um ponteiro para uma sequência de comprimento zero. 
  
## <a name="see-also"></a>Confira também



[IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)
  
[IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md)
  
[MSGSERVICEENTRY](msgserviceentry.md)
  
[IProfAdmin : IUnknown](iprofadminiunknown.md)

