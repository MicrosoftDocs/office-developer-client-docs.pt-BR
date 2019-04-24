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
ms.openlocfilehash: 288e34a159db48b1344524b87f02b045259f1565
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315292"
---
# <a name="ulrelease"></a>UlRelease

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Fornece uma maneira alternativa para invocar o método OLE **IUnknown:: Release**. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs. h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos cliente e provedores de serviços  <br/> |
   
```cpp
ULONG UlRelease(
  LPVOID punk
);
```

## <a name="parameters"></a>Parâmetros

 _punk_
  
> no Ponteiro para uma interface derivada da interface **IUnknown** , em outras palavras, em qualquer interface MAPI. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada teve êxito e retornou o valor ou valores esperados. 
    
MAPI_E_CALL_FAILED 
  
> Um erro de origem inesperada ou desconhecida impediu a conclusão da operação.
    
## <a name="remarks"></a>Comentários

A contagem de referência é o número de ponteiros existentes para o objeto a ser liberado. 
  
Se o parâmetro _punk_ for NULL, a função retornará imediatamente sem chamar **IUnknown:: Release**
  
 **UlRelease** retorna o valor retornado pelo método **IUnknown:: Release** , que pode ser igual à contagem de referência do objeto a ser liberado. 
  
Para obter mais informações sobre o **IUnknown:: Release**, consulte [Implementing the IUnknown interface](implementing-the-iunknown-interface.md). 
  

