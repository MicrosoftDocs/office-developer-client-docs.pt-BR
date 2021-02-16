---
title: UlAddRef
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.UlAddRef
api_type:
- COM
ms.assetid: 9b897cbc-90b2-4c60-b5f1-dc78e7e7952d
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: f9e55153830dbe41a2b4a48454157c900d96cf90
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432832"
---
# <a name="uladdref"></a>UlAddRef

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Fornece uma maneira alternativa de invocar o método OLE **IUnknown::AddRef**. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos cliente e provedores de serviços  <br/> |
   
```cpp
ULONG UlAddRef(
  LPVOID punk
);
```

## <a name="parameters"></a>Parâmetros

 _2013_
  
> [in] Ponteiro para uma interface derivada da interface **IUnknown,** ou seja, qualquer interface MAPI. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor ou os valores esperados. 
    
MAPI_E_CALL_FAILED 
  
> Um erro de origem inesperada ou desconhecida impedia a conclusão da operação.
    
## <a name="remarks"></a>Comentários

 **UlAddRef** retorna o valor retornado pelo método **IUnknown::AddRef,** que é o novo valor da contagem de referência da interface. O valor é não zero. 
  
Para obter mais informações **sobre IUnknown::AddRef**, consulte [Implementando a interface IUnknown](implementing-the-iunknown-interface.md). 
  

