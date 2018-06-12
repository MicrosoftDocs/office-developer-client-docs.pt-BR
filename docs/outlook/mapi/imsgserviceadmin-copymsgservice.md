---
title: IMsgServiceAdminCopyMsgService
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.CopyMsgService
api_type:
- COM
ms.assetid: a13c6757-358f-421a-9a76-de7483501613
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: d9a15abc05bf0f0a6fef35dd489f12925b88014a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767483"
---
# <a name="imsgserviceadmincopymsgservice"></a>IMsgServiceAdmin::CopyMsgService

  
  
**Aplica-se a**: Outlook 
  
Copia um serviço de mensagem para um perfil. 
  
```cpp
HRESULT CopyMsgService(
  LPMAPIUID lpUID,
  LPSTR lpszDisplayName,
  LPCIID lpInterfaceToCopy,
  LPCIID lpInterfaceDst,
  LPVOID lpObjectDst,
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Par�metros

 _lpUID_
  
> [in] Um ponteiro para a estrutura [MAPIUID](mapiuid.md) que contém o identificador exclusivo do serviço de mensagem para copiar. 
    
 _lpszDisplayName_
  
> [in] Esse parâmetro foi reduzido. 
    
 _lpInterfaceToCopy_
  
> [in] Um ponteiro para o identificador de interface (IID) que representa a interface que será usada para acessar a seção de perfil do serviço de mensagem para copiar. Passagem nula resulta no perfil padrão seção interface [IProfSect](iprofsectimapiprop.md), que está sendo utilizada.
    
 _lpInterfaceDst_
  
> [in] Um ponteiro para a IID que representa a interface que será usada para acessar o objeto apontado pelo parâmetro _lpObjectDst_ . Passagem nula resulta na interface de sessão, [IMAPISession](imapisessioniunknown.md), sendo usada. O parâmetro _lpInterfaceDst_ também pode ser definido como IID_IMsgServiceAdmin. 
    
 _lpObjectDst_
  
> [in] Um ponteiro para um ponteiro para um objeto de administração de serviço de sessão ou mensagem. O tipo de objeto deve corresponder ao identificador de interface passado em _lpInterfaceDst_. Ponteiros de objeto válido são LPMAPISESSION e LPSERVICEADMIN.
    
 _ulUIParam_
  
> [in] Um identificador para a janela do pai de quaisquer caixas de diálogo ou windows esse método exibe.
    
 _ulFlags_
  
> [in] Uma bitmask dos sinalizadores que controla como o serviço de mensagem é copiado. Sinalizadores a seguir podem ser definidos:
    
SERVICE_UI_ALWAYS 
  
> Solicita que o serviço de mensagem sempre exibe uma folha de propriedades de configuração.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> O serviço de mensagem foi copiado com êxito.
    
MAPI_E_NO_ACCESS 
  
> O serviço de mensagem já está no perfil e não permitir que várias instâncias de si mesmo.
    
E_NOT_FOUND 
  
> **MAPIUID** apontado pela _lpUID_ não faz referência a um serviço de mensagem existente. 
    
## <a name="remarks"></a>Coment�rios

O método **IMsgServiceAdmin::CopyMsgService** copia um serviço de mensagem para um perfil, o perfil ativo ou outro perfil. O perfil que contém o serviço de mensagem a ser copiado e o destino não precisam ser o mesmo perfil, mas eles podem ser. 
  
Função do ponto de entrada do serviço de mensagem não é chamada para uma operação de cópia. O serviço de mensagem copiada tem as mesmas definições de configuração do seu original. Para alterar essas configurações, um cliente deve chamar o método [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) . 
  
## <a name="see-also"></a>Confira também



[IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)
  
[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin: IUnknown](imsgserviceadminiunknown.md)

