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
ms.openlocfilehash: 822b4164737aa6010ccce108b544410104ac023d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415128"
---
# <a name="ipstoverride1getpersistedregistrations"></a>IPSTOVERRIDE1::GetPersistedRegistrations

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Recupera a lista de registros do arquivo de Pastas Particulares (.pst).
  
```cpp
HRESULT GetPersistedRegistration(SPropValue **ppmval);
```

## <a name="parameters"></a>Parâmetros

 _ppmval_
  
> [in] Um ponteiro para um ponteiro para uma [estrutura SPropValue.](spropvalue.md) O membro ulPropTag dessa estrutura é do tipo PT_MV_UNICODE, e o membro de valor MVszW será uma matriz de cadeias de caracteres Unicode terminadas por caractere nulo. Essas cadeias de caracteres são caminhos para DLLs para os quais o registro foi persistente. 
    
> [!NOTE]
> O suporte ao .pst para ANSI não foi implementado. 
  
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada de função foi bem-sucedida.
    
## <a name="see-also"></a>Confira também



[IPSTOVERRIDE1 : IUnknown](ipstoverride1iunknown.md)
  
[IPSTOVERRIDEREQ : IUnknown](ipstoverridereqiunknown.md)

