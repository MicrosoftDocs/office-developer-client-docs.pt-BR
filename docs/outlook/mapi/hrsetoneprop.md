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
ms.openlocfilehash: 31d2be027ef3b58fdd44e71c922677164d352feb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569124"
---
# <a name="hrsetoneprop"></a>HrSetOneProp

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Define ou altera o valor de uma única propriedade em uma interface de propriedade, ou seja, uma interface derivada [IMAPIProp](imapipropiunknown.md). 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil.h  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Provedores de serviços e aplicativos cliente  <br/> |
   
```cpp
HrSetOneProp(
  LPMAPIPROP pmp,
  LPSPropValue pprop
);
```

## <a name="parameters"></a>Parâmetros

 _PMP_
  
> [in] Ponteiro para uma interface de [IMAPIProp](imapipropiunknown.md) em que o valor da propriedade deve ser definida ou alterada. 
    
 _pprop_
  
> [in] Ponteiro para a estrutura de [SPropValue](spropvalue.md) definindo o valor a ser definido na propriedade _pmp_ . 
    
## <a name="return-value"></a>Valor retornado

Nenhum.
  
## <a name="remarks"></a>Comentários

Ao contrário do método [IMAPIProp::SetProps](imapiprop-setprops.md) , a função **HrSetOneProp** nunca retorna todos os avisos. Porque ele define apenas uma propriedade, ele simplesmente for bem-sucedido ou falha. Para definir ou alterar várias propriedades, **SetProps** é mais rápido. 
  
É possível recuperar uma única propriedade com a função [HrGetOneProp](hrgetoneprop.md) . 
  

