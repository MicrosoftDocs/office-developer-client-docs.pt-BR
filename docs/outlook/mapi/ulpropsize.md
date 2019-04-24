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
ms.openlocfilehash: cc1547ad7d881b707825630f96987d4c40ad4863
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315299"
---
# <a name="ulpropsize"></a>UlPropSize

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Retorna o tamanho de um único valor de propriedade. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs. h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos cliente e provedores de serviços  <br/> |
   
```cpp
ULONG UlPropSize(
  LPSPropValue lpSPropValue
);
```

## <a name="parameters"></a>Parâmetros

 _lpSPropValue_
  
> no Ponteiro para uma estrutura [SPropValue](spropvalue.md) que define a propriedade a ser medida. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada teve êxito e retornou o valor ou valores esperados. 
    
MAPI_E_CALL_FAILED 
  
> Um erro de origem inesperada ou desconhecida impediu a conclusão da operação.
    
## <a name="remarks"></a>Comentários

A função **UlPropSize** retorna o tamanho, em bytes, do valor da propriedade especificada. Ele ignora o tamanho do restante da estrutura **SPropValue** . 
  

