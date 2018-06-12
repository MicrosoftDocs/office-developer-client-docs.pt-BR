---
title: IContabAdminRemoveStore
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IContabAdmin.RemoveStore
api_type:
- COM
ms.assetid: 2a5fcf5c-8a5a-4774-b8c9-1ac1ff27947d
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 868f38eaf52d3d0a3787623983a4a587de8fdc3b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766896"
---
# <a name="icontabadminremovestore"></a>IContabAdmin::RemoveStore

  
  
**Aplica-se a**: Outlook 
  
Remove o contato endereço CAB (catálogo) especificado pela ID de entrada determinada da hierarquia de catálogo de endereços.
  
```cpp
HRESULT RemoveStore(
ULONG cbEntryID, 
LPENTRYID lpEntryID
);
```

## <a name="parameters"></a>Par�metros

 _cbEntryID_
  
> [in] A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID_ . 
    
 _lpEntryID_
  
> [in] Um ponteiro para o identificador de entrada do objeto a ser aberto.
    

