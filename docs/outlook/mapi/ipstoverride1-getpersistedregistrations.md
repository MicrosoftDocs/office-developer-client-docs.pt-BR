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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 56aaf5caf93f90f54d152ab3684ca592cd45cd1c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767655"
---
# <a name="ipstoverride1getpersistedregistrations"></a>IPSTOVERRIDE1::GetPersistedRegistrations

  
  
**Aplica-se a**: Outlook 
  
Recupera a lista dos registros para o arquivo de pastas particulares (. pst).
  
```cpp
HRESULT GetPersistedRegistration(SPropValue **ppmval);
```

## <a name="parameters"></a>Par�metros

 _ppmval_
  
> [in] Um ponteiro para um ponteiro para uma estrutura [SPropValue](spropvalue.md) . O membro ulPropTag esta estrutura é do tipo PT_MV_UNICODE e o membro de valor de MVszW será uma matriz de cadeias de caracteres de Unicode terminada em nulo. Essas cadeias de caracteres são caminhos para DLLs para o qual o registro tem foi persistente. 
    
> [!NOTE]
> suporte. pst para ANSI não está implementado. 
  
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A chamada de função foi bem-sucedida.
    
## <a name="see-also"></a>Confira também



[IPSTOVERRIDE1: IUnknown](ipstoverride1iunknown.md)
  
[IPSTOVERRIDEREQ: IUnknown](ipstoverridereqiunknown.md)

