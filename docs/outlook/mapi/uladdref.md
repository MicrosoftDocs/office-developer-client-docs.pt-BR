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
ms.openlocfilehash: baf45fa33ca085f51a6f9c20f72ec1fd1545ad79
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592365"
---
# <a name="uladdref"></a>UlAddRef

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Fornece uma maneira alternativa para invocar o método OLE **AddRef**. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Provedores de serviços e aplicativos cliente  <br/> |
   
```cpp
ULONG UlAddRef(
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

 **UlAddRef** retornará o valor retornado pelo método **AddRef** , que é o novo valor da contagem de referência para a interface. O valor é diferente de zero. 
  
Para obter mais informações sobre **AddRef**, consulte [Implementando a IUnknown Interface](implementing-the-iunknown-interface.md). 
  

