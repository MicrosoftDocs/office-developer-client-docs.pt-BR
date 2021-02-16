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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418719"
---
# <a name="getinstance"></a>GetInstance

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Copia um valor dentro de uma propriedade de múltiplos valores para uma propriedade de valor único do mesmo tipo. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |MAPIUTIL. H  <br/> |
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
  
> [in] Ponteiro para uma [estrutura SPropValue](spropvalue.md) definindo uma propriedade de múltiplos valores. 
    
 _pvalSv_
  
> [in] Ponteiro para uma propriedade de valor único para receber dados. 
    
 _uliInst_
  
> [in] O número da instância, ou seja, o elemento da matriz, do valor que está sendo copiado da estrutura indicada pelo _parâmetro pvalMv._ 
    
## <a name="return-value"></a>Valor retornado

Nenhum.
  
## <a name="remarks"></a>Comentários

Se o valor copiado for muito grande para a memória alocada, a função **GetInstance** só copiará ponteiros em vez de alocar nova memória. 
  

