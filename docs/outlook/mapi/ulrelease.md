---
title: UlRelease
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.UlRelease
api_type:
- COM
ms.assetid: 95db96ef-f95f-41da-b216-f717c23bffd2
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 5b34e2c21ac967b0874872986c0cf484750f4e72
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770660"
---
# <a name="ulrelease"></a>UlRelease

  
  
**Aplica-se a**: Outlook 
  
Fornece uma maneira alternativa para invocar o método OLE **IUnknown:: Release**. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Provedores de serviços e aplicativos cliente  <br/> |
   
```cpp
ULONG UlRelease(
  LPVOID punk
);
```

## <a name="parameters"></a>Parâmetros

 _punk_
  
> [in] Ponteiro para uma interface derivada da interface **IUnknown** , em outras palavras, qualquer interface MAPI. 
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores. 
    
MAPI_E_CALL_FAILED 
  
> Um erro de origem inesperado ou desconhecido impediu a conclusão da operação.
    
## <a name="remarks"></a>Comentários

A contagem de referência é o número de ponteiros existentes para o objeto ser liberada. 
  
Se o parâmetro _punk_ for NULL, a função retornará imediatamente sem chamar **IUnknown:: Release**
  
 **UlRelease** retornará o valor retornado pelo método **IUnknown:: Release** , que pode ser igual à contagem de referência para o objeto ser liberada. 
  
Para obter mais informações sobre **IUnknown:: Release**, consulte [Implementando a IUnknown Interface](implementing-the-iunknown-interface.md). 
  

