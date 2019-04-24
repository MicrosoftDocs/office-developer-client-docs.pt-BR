---
title: GetInstance
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.GetInstance
api_type:
- COM
ms.assetid: cb432d52-6c96-45d2-bbde-45b0de3f915c
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 936a20c4236ab76e5acdb178737c3044d3f53bfe
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299542"
---
# <a name="getinstance"></a>GetInstance

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Copia um valor dentro de uma propriedade de vários valores para uma propriedade de valor único do mesmo tipo. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |MAPIUTIL. 0  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos cliente e provedores de serviços  <br/> |
   
```cpp
VOID GetInstance(
  LPSPropValue pvalMv,
  LPSPropValue pvalSv,
  ULONG uliInst
);
```

## <a name="parameters"></a>Parâmetros

 _pvalMv_
  
> no Ponteiro para uma estrutura [SPropValue](spropvalue.md) que define uma propriedade de vários valores. 
    
 _pvalSv_
  
> no Ponteiro para uma propriedade de valor único para receber dados. 
    
 _uliInst_
  
> no O número da instância, ou seja, o elemento array, do valor que está sendo copiado da estrutura indicada pelo parâmetro _pvalMv_ . 
    
## <a name="return-value"></a>Valor retornado

Nenhum.
  
## <a name="remarks"></a>Comentários

Se o valor copiado for muito grande para a memória alocada **** , a função getInstance só copiará os ponteiros em vez de alocar uma nova memória. 
  

