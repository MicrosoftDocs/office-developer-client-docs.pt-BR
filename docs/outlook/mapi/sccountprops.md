---
title: ScCountProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScCountProps
api_type:
- COM
ms.assetid: 76e4cc52-e1a0-4e0b-a2a6-a17644f6b2e7
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 49634bda487143ddd8d8806b94f6c451ccf57b75
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404971"
---
# <a name="sccountprops"></a>ScCountProps

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Determina o tamanho, em bytes, de uma matriz de valores de propriedade e valida a memória associada à matriz. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos cliente e provedores de serviços  <br/> |
   
```cpp
SCODE ScCountProps(
  int cprop,
  LPSPropValue rgprop,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a>Parâmetros

 _cprop_
  
> [in] Contagem de propriedades na matriz indicada pelo _parâmetro rgprop._ 
    
 _rgprop_
  
> [in] Ponteiro para um intervalo em uma matriz [de estruturas SPropValue](spropvalue.md) que define as propriedades cujo tamanho deve ser determinado. Esse intervalo não começa necessariamente no início da matriz. 
    
 _pcb_
  
> [out] Ponteiro opcional para o tamanho, em bytes, da matriz de propriedades.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor ou os valores esperados. 
    
MAPI_E_INVALID_PARAMETER 
  
> Pelo menos uma propriedade na matriz de valores de propriedade tem um identificador de PROP_ID_NULL ou PROP_ID_INVALID, ou a matriz de propriedades contém uma propriedade de múltiplos valores sem valores de propriedade.
    
## <a name="remarks"></a>Comentários

Se NULL for passado no parâmetro  _pcb,_ a função **ScCountProps** validará a matriz de notificações, mas nenhuma contagem será feita. Se um valor não nulo for passado em  _pcb_, a função **ScCountNotifications** determinará o tamanho da matriz e armazenará a causa  _pcb_. O  _parâmetro pcb_ deve ser grande o suficiente para conter toda a matriz. 
  
Enquanto está contando, **ScCountProps** valida a memória associada à matriz. **ScCountProps** só funciona com propriedades sobre as quais MAPI tem informações. 
  
## <a name="see-also"></a>Confira também



[PropCopyMore](propcopymore.md)

