---
title: IMAPISupportSetProviderUID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.SetProviderUID
api_type:
- COM
ms.assetid: 58855843-9a2b-4e5d-9332-b1bfad8b45e4
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: a60ac0d7ab139f77aea87080e1ce37fee870e97b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326310"
---
# <a name="imapisupportsetprovideruid"></a>IMAPISupport::SetProviderUID

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Registra uma estrutura [MAPIUID](mapiuid.md) que representa exclusivamente o provedor de serviços. 
  
```cpp
HRESULT SetProviderUID(
LPMAPIUID lpProviderID,
ULONG ulFlags
);
```

## <a name="parameters"></a>Parâmetros

 _lpProviderID_
  
> no Um ponteiro para a estrutura **MAPIUID** que identifica o catálogo de endereços ou o provedor de repositório de mensagens. 
    
 _ulFlags_
  
> Serve deve ser zero.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A estrutura **MAPIUID** foi registrada com êxito. 
    
## <a name="remarks"></a>Comentários

O método **IMAPISupport:: SetProviderUID** é implementado para o catálogo de endereços e os objetos de suporte do provedor de repositório de mensagens. Esses provedores chamam **SetProviderUID** para registrar um identificador exclusivo descrito na estrutura **MAPIUID** indicada por _lpProviderID_. Os provedores incluem esse identificador em todos os identificadores de entrada criados por eles. 
  
MAPI usa a estrutura **MAPIUID** quando ele envia mensagens de saída para o spooler MAPI e para determinar o provedor apropriado para lidar com solicitações de cliente. Por exemplo, quando um cliente chama o método [IMAPISession:: OpenEntry](imapisession-openentry.md) , o MAPI examina a parte **MAPIUID** do identificador de entrada, mapeia-o para o provedor que o aprovou para **SetProviderUID**e chama o **OpenEntry** do provedor . 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Chame **SetProviderUID** no momento do logon para registrar sua estrutura do **MAPIUID** . MAPI permite que o catálogo de endereços e provedores de repositório de mensagens registrem vários identificadores. Quando você faz várias chamadas para o **SetProviderUID**, ela sempre adiciona a estrutura **MAPIUID** ao conjunto de estruturas **MAPIUID** do provedor, mesmo que o **MAPIUID** seja uma duplicata. **SetProviderUID** não pode remover um **MAPIUID**. 
  
## <a name="see-also"></a>Confira também



[MAPIUID](mapiuid.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

