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
ms.openlocfilehash: 8af0d5c6eaff0c1e01e01c24c46f299e0c637f68
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766812"
---
# <a name="hrsetoneprop"></a>HrSetOneProp

  
  
**Aplica-se a**: Outlook 
  
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
  

