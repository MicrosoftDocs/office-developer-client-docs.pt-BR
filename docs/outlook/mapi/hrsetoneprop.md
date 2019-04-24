---
title: HrSetOneProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrSetOneProp
api_type:
- COM
ms.assetid: 14ae3242-fddf-4199-a9a7-4ab153b31064
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 37e6560d859ce4731b7a06e571eb38eb160c3686
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32347765"
---
# <a name="hrsetoneprop"></a>HrSetOneProp

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Define ou altera o valor de uma única propriedade em uma interface de propriedade, ou seja, uma interface derivada de [IMAPIProp](imapipropiunknown.md). 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil. h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos cliente e provedores de serviços  <br/> |
   
```cpp
HrSetOneProp(
  LPMAPIPROP pmp,
  LPSPropValue pprop
);
```

## <a name="parameters"></a>Parâmetros

 _PMP_
  
> no Ponteiro para uma interface [IMAPIProp](imapipropiunknown.md) na qual o valor da propriedade deve ser definido ou alterado. 
    
 _pProp_
  
> no Ponteiro para a estrutura [SPropValue](spropvalue.md) que define o valor a ser definido na propriedade _PMP_ . 
    
## <a name="return-value"></a>Valor retornado

Nenhum.
  
## <a name="remarks"></a>Comentários

Diferentemente do método [IMAPIProp::](imapiprop-setprops.md) SetProps, a função **HrSetOneProp** nunca retorna quaisquer avisos. Como ela define apenas uma propriedade, ela simplesmente sucede ou falha. Para definir ou alterar várias propriedades, **** SetProps é mais rápido. 
  
Você pode recuperar uma única propriedade com a função [HrGetOneProp](hrgetoneprop.md) . 
  

