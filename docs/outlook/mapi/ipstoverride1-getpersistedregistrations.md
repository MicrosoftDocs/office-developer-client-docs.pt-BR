---
title: IPSTOVERRIDE1GetPersistedRegistrations
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTOVERRIDE1.GetPersistedRegistrations
api_type:
- COM
ms.assetid: 027092f0-f2d6-49e8-a8d0-8926824953a2
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 548ec33e39e181aba8a72b5325f3f426b9d51762
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575865"
---
# <a name="ipstoverride1getpersistedregistrations"></a>IPSTOVERRIDE1::GetPersistedRegistrations

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Recupera a lista dos registros para o arquivo de pastas particulares (. pst).
  
```cpp
HRESULT GetPersistedRegistration(SPropValue **ppmval);
```

## <a name="parameters"></a>Parâmetros

 _ppmval_
  
> [in] Um ponteiro para um ponteiro para uma estrutura [SPropValue](spropvalue.md) . O membro ulPropTag esta estrutura é do tipo PT_MV_UNICODE e o membro de valor de MVszW será uma matriz de cadeias de caracteres de Unicode terminada em nulo. Essas cadeias de caracteres são caminhos para DLLs para o qual o registro tem foi persistente. 
    
> [!NOTE]
> suporte. pst para ANSI não está implementado. 
  
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada de função foi bem-sucedida.
    
## <a name="see-also"></a>Confira também



[IPSTOVERRIDE1 : IUnknown](ipstoverride1iunknown.md)
  
[IPSTOVERRIDEREQ : IUnknown](ipstoverridereqiunknown.md)

