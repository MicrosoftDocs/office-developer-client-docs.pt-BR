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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: a15561a6f3af35c1c7c2285bb6252e6400e0e8df
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767620"
---
# <a name="iprofadmincreateprofile"></a>IProfAdmin::CreateProfile

  
  
**Aplica-se a**: Outlook 
  
Cria um novo perfil.
  
```cpp
HRESULT CreateProfile(
  LPSTR lpszProfileName,
  LPSTR lpszPassword,
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Par�metros

 _lpszProfileName_
  
> [in] Um ponteiro para o nome do novo perfil.
    
 _lpszPassword_
  
> [in] Um ponteiro para a senha do novo perfil. 
    
 _ulUIParam_
  
> [in] Um identificador para a janela pai de todas as caixas de diálogo ou windows que esse método exibe.
    
 _ulFlags_
  
> [in] Uma bitmask dos sinalizadores que controla como o perfil é criado. Sinalizadores a seguir podem ser definidos:
    
MAPI_DEFAULT_SERVICES 
  
> MAPI deve preencher o novo perfil com os serviços de mensagem que estão incluídos na seção [padrão Services] do arquivo Mapisvc.
    
MAPI_DIALOG 
  
> Podem ser exibidas as folhas de propriedades de configuração de cada um dos provedores nos serviços de mensagem a ser adicionado. 
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> O novo perfil foi criado.
    
MAPI_E_NO_ACCESS 
  
> O novo perfil especificado já existe.
    
## <a name="remarks"></a>Coment�rios

O método **IProfAdmin::CreateProfile** cria um novo perfil. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Você pode chamar **CreateProfile** no momento da instalação de aplicativos ou a qualquer momento durante uma sessão. Quando esse método é chamado no momento da instalação, muitas das definições de configuração provenientes do arquivo de configuração Mapisvc. Quando esse método é chamado durante uma sessão ativa, as configurações são provenientes de usuário que será solicitado por uma série de folhas de propriedades. 
  
Se o sinalizador MAPI_DEFAULT_SERVICES é definido no parâmetro _ulFlags_ , **CreateProfile** chama a função de ponto de entrada de serviço de mensagem para cada serviço de mensagem na seção [padrão Services] no arquivo Mapisvc. Cada função de ponto de entrada de serviço de mensagem é chamada com o parâmetro _ulContext_ definido como MSG_SERVICE_CREATE. 
  
Se flags MAPI_DIALOG tanto o MAPI_DEFAULT_SERVICES estiverem definidas, os valores nos parâmetros _ulUIParam_ e _ulFlags_ também são passados para a função de ponto de entrada de serviço de mensagem. As funções de ponto de entrada de serviço de mensagem são chamadas somente depois que todas as informações disponíveis do arquivo Mapisvc foi adicionadas ao perfil. 
  
O nome do novo perfil e sua senha pode ter até 64 caracteres de comprimento e pode incluir os seguintes caracteres:
  
- Todos os caracteres alfanuméricos, incluindo o caractere de sublinhado e ênfase.
    
- Espaços incorporados, mas não espaços à esquerda ou à direita.
    
O parâmetro _lpszPassword_ deve ser NULL ou um ponteiro para uma cadeia de caracteres de comprimento zero. 
  
## <a name="see-also"></a>Confira também



[IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)
  
[IMsgServiceAdmin:: CreateMsgService](imsgserviceadmin-createmsgservice.md)
  
[MSGSERVICEENTRY](msgserviceentry.md)
  
[IProfAdmin: IUnknown](iprofadminiunknown.md)

