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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309965"
---
# <a name="imsgserviceadmincopymsgservice"></a>IMsgServiceAdmin::CopyMsgService

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Copia um serviço de mensagens em um perfil. 
  
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
  
> no Um ponteiro para a estrutura [MAPIUID](mapiuid.md) que contém o identificador exclusivo do serviço de mensagens a ser copiado. 
    
 _lpszDisplayName_
  
> no Esse parâmetro foi preterido. 
    
 _lpInterfaceToCopy_
  
> no Um ponteiro para o identificador de interface (IID) que representa a interface a ser usada para acessar a seção de perfil do serviço de mensagens a ser copiada. Passar resultados nulos na interface de seção de perfil padrão, [IProfSect](iprofsectimapiprop.md), que está sendo usada.
    
 _lpInterfaceDst_
  
> no Um ponteiro para o IID que representa a interface a ser usada para acessar o objeto apontado pelo parâmetro _lpObjectDst_ . Passar resultados nulos na interface de sessão, [IMAPISession](imapisessioniunknown.md), sendo usado. O parâmetro _lpInterfaceDst_ também pode ser definido como IID_IMsgServiceAdmin. 
    
 _lpObjectDst_
  
> no Um ponteiro para um ponteiro para um objeto de administração de sessão ou serviço de mensagens. O tipo de objeto deve corresponder ao identificador de interface passado no _lpInterfaceDst_. Os ponteiros de objeto válidos são LPMAPISESSION e LPSERVICEADMIN.
    
 _ulUIParam_
  
> no Uma alça para a janela pai de qualquer caixa de diálogo ou Windows este método é exibido.
    
 _ulFlags_
  
> no Uma bitmask de sinalizadores que controla como o serviço de mensagens é copiado. Os seguintes sinalizadores podem ser definidos:
    
SERVICE_UI_ALWAYS 
  
> Solicita que o serviço de mensagens sempre exiba uma folha de propriedades de configuração.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O serviço de mensagens foi copiado com êxito.
    
MAPI_E_NO_ACCESS 
  
> O serviço de mensagens já está no perfil e não permite várias instâncias de si mesmo.
    
MAPI_E_NOT_FOUND 
  
> O **MAPIUID** apontado por _lpUID_ não se refere a um serviço de mensagens existente. 
    
## <a name="remarks"></a>Comentários

O método **IMsgServiceAdmin:: CopyMsgService** copia um serviço de mensagem em um perfil, seja o perfil ativo ou outro perfil. O perfil que contém o serviço de mensagens a ser copiado e o destino não precisam ser o mesmo perfil, mas podem ser. 
  
A função de ponto de entrada do serviço de mensagens não é chamada para uma operação de cópia. O serviço de mensagens copiadas tem as mesmas definições de configuração que o original. Para alterar essas configurações, um cliente deve chamar o método [IMsgServiceAdmin:: ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) . 
  
## <a name="see-also"></a>Confira também



[IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)
  
[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)

