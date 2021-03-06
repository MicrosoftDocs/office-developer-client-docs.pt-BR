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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417655"
---
# <a name="hrsetoneprop"></a>HrSetOneProp

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Define ou altera o valor de uma única propriedade em uma interface de propriedade, ou seja, uma interface derivada de [IMAPIProp](imapipropiunknown.md). 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos cliente e provedores de serviços  <br/> |
   
```cpp
HrSetOneProp(
  LPMAPIPROP pmp,
  LPSPropValue pprop
);
```

## <a name="parameters"></a>Parâmetros

 _pmp_
  
> [in] Ponteiro para uma interface [IMAPIProp](imapipropiunknown.md) na qual o valor da propriedade deve ser definido ou alterado. 
    
 _pprop_
  
> [in] Ponteiro para a [estrutura SPropValue](spropvalue.md) definindo o valor a ser definido na _propriedade pmp._ 
    
## <a name="return-value"></a>Valor retornado

Nenhum.
  
## <a name="remarks"></a>Comentários

Ao contrário [do método IMAPIProp::SetProps,](imapiprop-setprops.md) **a função HrSetOneProp** nunca retorna nenhum aviso. Como define apenas uma propriedade, ela simplesmente é bem-sucedida ou falha. Para definir ou alterar várias propriedades, **SetProps** é mais rápido. 
  
Você pode recuperar uma única propriedade com a [função HrGetOneProp.](hrgetoneprop.md) 
  

