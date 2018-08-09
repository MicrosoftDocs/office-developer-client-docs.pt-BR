---
title: UlPropSize
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.UlPropSize
api_type:
- COM
ms.assetid: 240f1144-0805-4cd1-9e7d-f2a550a2f160
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: bc00270b167c9f7317fa466d790d5020d961676f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770643"
---
# <a name="ulpropsize"></a>UlPropSize

  
  
**Aplica-se a**: Outlook 
  
Retorna o tamanho de um valor de propriedade exclusivo. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Provedores de serviços e aplicativos cliente  <br/> |
   
```cpp
ULONG UlPropSize(
  LPSPropValue lpSPropValue
);
```

## <a name="parameters"></a>Parâmetros

 _lpSPropValue_
  
> [in] Ponteiro para uma estrutura [SPropValue](spropvalue.md) definindo a propriedade a ser medido. 
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores. 
    
MAPI_E_CALL_FAILED 
  
> Um erro de origem inesperado ou desconhecido impediu a conclusão da operação.
    
## <a name="remarks"></a>Comentários

A função **UlPropSize** retorna o tamanho, em bytes, do valor da propriedade para a propriedade especificada. Ele ignora o tamanho do restante da estrutura **SPropValue** . 
  

