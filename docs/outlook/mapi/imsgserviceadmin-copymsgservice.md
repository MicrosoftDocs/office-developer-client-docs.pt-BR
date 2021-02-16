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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 72b4ab1fec10b2e91c7609af6644a54d29ed5e02
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432118"
---
# <a name="imsgserviceadmincopymsgservice"></a>IMsgServiceAdmin::CopyMsgService

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Copia um serviço de mensagens para um perfil. 
  
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

## <a name="parameters"></a>Parâmetros

 _lpUID_
  
> [in] Um ponteiro para a [estrutura MAPIUID](mapiuid.md) que contém o identificador exclusivo do serviço de mensagens a ser copiado. 
    
 _lpszDisplayName_
  
> [in] Esse parâmetro foi preterido. 
    
 _lpInterfaceToCopy_
  
> [in] Um ponteiro para o IID (identificador de interface) que representa a interface a ser usada para acessar a seção de perfil do serviço de mensagens a ser copiado. Passar resultados NULL na interface da seção de perfil padrão, [IProfSect](iprofsectimapiprop.md), sendo usado.
    
 _lpInterfaceDst_
  
> [in] Um ponteiro para a IID que representa a interface a ser usada para acessar o objeto apontado pelo parâmetro _lpObjectDst._ Passar resultados NULL na interface de sessão, [IMAPISession](imapisessioniunknown.md), sendo usado. O  _parâmetro lpInterfaceDst_ também pode ser definido como IID_IMsgServiceAdmin. 
    
 _lpObjectDst_
  
> [in] Um ponteiro para um ponteiro para um objeto de administração de serviço de mensagens ou sessão. O tipo de objeto deve corresponder ao identificador de interface passado  _em lpInterfaceDst_. Ponteiros de objeto válidos são LPMAPISESSION e LPSERVICEADMIN.
    
 _ulUIParam_
  
> [in] Um alça para a janela pai de quaisquer caixas de diálogo ou janelas que esse método exibe.
    
 _ulFlags_
  
> [in] Uma máscara de bits de sinalizadores que controla como o serviço de mensagens é copiado. Os sinalizadores a seguir podem ser definidos:
    
SERVICE_UI_ALWAYS 
  
> Solicita que o serviço de mensagens sempre exibe uma folha de propriedades de configuração.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O serviço de mensagens foi copiado com êxito.
    
MAPI_E_NO_ACCESS 
  
> O serviço de mensagens já está no perfil e não permite várias instâncias de si mesmo.
    
MAPI_E_NOT_FOUND 
  
> O **MAPIUID** apontado por  _lpUID_ não se refere a um serviço de mensagens existente. 
    
## <a name="remarks"></a>Comentários

O **método IMsgServiceAdmin::CopyMsgService** copia um serviço de mensagens para um perfil, seja o perfil ativo ou outro perfil. O perfil que contém o serviço de mensagens a ser copiado e o destino não precisa ser o mesmo perfil, mas pode ser. 
  
A função de ponto de entrada do serviço de mensagens não é chamada para uma operação de cópia. O serviço de mensagens copiado tem as mesmas definições de configuração que o original. Para alterar essas configurações, um cliente deve chamar o [método IMsgServiceAdmin::ConfigureMsgService.](imsgserviceadmin-configuremsgservice.md) 
  
## <a name="see-also"></a>Confira também



[IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)
  
[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)

