---
title: IMsgServiceAdmin2CreateMsgServiceEx
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin2.CreateMsgServiceEx
api_type:
- COM
ms.assetid: 4910dabd-9380-4fde-a440-5c64d74c0bba
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 3aae61f7b21c507da7955dbb4393d13bfb5fa24c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767473"
---
# <a name="imsgserviceadmin2createmsgserviceex"></a>IMsgServiceAdmin2::CreateMsgServiceEx

  
  
**Aplica-se a**: Outlook 
  
Adiciona um serviço de mensagem para o perfil atual e a retorna que tenha sido adicionado recentemente UID do serviço.
  
```cpp
HRESULT CreateMsgServiceEx(
  LPSTR lpszService,
  LPSTR lpszDisplayName,
  ULONG_PTR ulUIParam,
  ULONG ulFlags,    
  LPMAPIUID lpuidService
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
    
 _lpuidService_
  
> [out] O ponteiro para o UID do serviço de mensagem adicionado.
    
## <a name="return-value"></a>Valor retornado

S_OK
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores.
    
E_NOT_FOUND
  
> O nome do serviço de mensagem não está na seção **[Services]** da Mapisvc. 
    
## <a name="remarks"></a>Comentários

O método **IMsgServiceAdmin2::CreateMsgServiceEx** adiciona um serviço de mensagem ao perfil atual. **CreateMsgServiceEx** chama a função de ponto de entrada do serviço de mensagem para executar tarefas específicas do serviço de configuração. Se o sinalizador SERVICE_UI_ALLOWED é definido no parâmetro _ulFlags_ , o serviço de mensagem que está sendo instalado pode exibir uma folha de propriedades, permitindo ao usuário definir suas configurações. 
  
O arquivo Mapisvc contém uma lista de provedores que compõem um serviço de mensagem e as propriedades para cada um. **CreateMsgServiceEx** primeiro cria uma nova seção de perfil para o serviço de mensagem e, em seguida, copia todas as informações para o serviço do arquivo Mapisvc exe para o perfil, criando novas seções para cada provedor. 
  
Depois que todas as informações foram copiadas dos Mapisvc, a função de ponto de entrada do serviço de mensagem, **MSGSERVICEENTRY**, é chamada com o valor MSG_SERVICE_CREATE definido no parâmetro _ulContext_ . Se o sinalizador SERVICE_UI_ALLOWED é definido no parâmetro de _ulFlags_ do método **CreateMsgServiceEx** , os valores nos parâmetros _ulUIParam_ e _ulFlags_ também são passados quando a função de ponto de entrada do serviço de mensagem é chamada. Provedores de serviços devem exibir suas folhas de propriedades de configuração para que os usuários podem configurar o serviço de mensagem. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Se o argumento de _lpuidService_ **CreateMsgServiceEx** não for nulo, a propriedade **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) do serviço de mensagem que foi adicionada ao perfil é retornada o **GUID** para o qual ela aponta. 
  
Passe o valor da propriedade **PR_SERVICE_UID** no parâmetro _lpuidService_ para o método [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) para configurar o serviço. 
  
> [!CAUTION]
> A implementação do Microsoft Outlook 2010 do subsistema de MAPI não suporta MAPI_UNICODE e irá falhar se for usado. 
  
> [!IMPORTANT]
> A interface IMsgServiceAdmin2 é exposta pelo mesmo objeto que implementa a interface IMsgServiceAdmin e está disponível por meio da implementação do Outlook do subsistema de MAPI desde o Outlook 2003. Seu IID é definido conforme segue: > `#if !defined(INITGUID) || defined(USES_IID_IMsgServiceAdmin2)` >   `DEFINE_OLEGUID(IID_IMsgServiceAdmin2,0x00020387, 0, 0);`> _ulFlags_ SERVICE_NO_RESTART_WARNING não podem ser definidos no arquivo de cabeçalho para download que você possui atualmente, nesse caso, você pode adicioná-lo para seu código usando o seguinte valor: >`#define SERVICE_NO_RESTART_WARNING 0x00000080`
  
## <a name="see-also"></a>Confira também



[IMsgServiceAdmin2 : IMsgServiceAdmin](imsgserviceadmin2imsgserviceadmin.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)

