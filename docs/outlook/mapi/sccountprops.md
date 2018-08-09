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
ms.openlocfilehash: 97dad50fed4179526e46381c4d9ea9d12d568377
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770338"
---
# <a name="sccountprops"></a>ScCountProps

  
  
**Aplica-se a**: Outlook 
  
Determina o tamanho, em bytes, de uma matriz de valores de propriedade e valida a memória associada a matriz. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil.h  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Provedores de serviços e aplicativos cliente  <br/> |
   
```cpp
SCODE ScCountProps(
  int cprop,
  LPSPropValue rgprop,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a>Parâmetros

 _cprop_
  
> [in] Contagem de propriedades na matriz indicado pelo parâmetro _rgprop_ . 
    
 _rgprop_
  
> [in] Ponteiro para um intervalo em uma matriz de estruturas de [SPropValue](spropvalue.md) que define as propriedades cujo tamanho é seja determinado. Esse intervalo não necessariamente inicia no início da matriz. 
    
 _PCB_
  
> [out] Ponteiro opcional para o tamanho, em bytes, de matriz de propriedades.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores. 
    
MAPI_E_INVALID_PARAMETER 
  
> Pelo menos uma propriedade da matriz de valores de propriedade tem um identificador de PROP_ID_NULL ou PROP_ID_INVALID ou a matriz de propriedade contém uma propriedade de vários valores sem valores de propriedade.
    
## <a name="remarks"></a>Comentários

Se NULL é passada no parâmetro _pcb_ , a função **ScCountProps** valida a matriz de notificações, mas nenhum contando é feito. Se um valor não-nulo é passado _pcb_, a função **ScCountNotifications** determina o tamanho da matriz e armazena a causa _pcb_. O parâmetro _pcb_ deve ser grande o suficiente para conter toda a matriz. 
  
Conforme ele está contando, **ScCountProps** valida a memória associada a matriz. **ScCountProps** funciona apenas com sobre quais MAPI tem informações de propriedades. 
  
## <a name="see-also"></a>Confira também



[PropCopyMore](propcopymore.md)

