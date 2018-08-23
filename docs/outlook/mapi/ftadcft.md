---
title: FtAdcFt
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2635a829-0f3a-49ed-a672-2f350a2cf979
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: f073dbb9655585ee56ab38be35bea4ef320042c0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569768"
---
# <a name="ftadcft"></a>FtAdcFt

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Adiciona um inteiro não assinado de 64 bits para outro, opcionalmente, usando um sinalizador pode executar.
  
|||
|:-----|:-----|
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Provedores de serviços e aplicativos cliente  <br/> |
   
```cpp
FILETIME FtAdcFt( 
  FILETIME ft1, 
  FILETIME ft2, 
  WORD FAR *pwCarry
);
```

## <a name="parameters"></a>Parâmetros

 _FT1_
  
> [in] Uma estrutura [FILETIME](filetime.md) que contém o primeiro inteiro não assinado de 64 bits a ser adicionado. 
    
 _ft2_
  
> [in] Uma estrutura FILETIME que contém o segundo inteiro não assinado de 64 bits a ser adicionado.
    
 _pwCarry_
  
> [in, check-out, opcional] Na entrada, um ponteiro de entrada transportar sinalizador. Na saída, um ponteiro para o resultado deve executar a adição. Esse parâmetro pode ser NULL se o resultado deve executar não é necessário.
    
## <a name="return-value"></a>Valor retornado

A função **FtAdcFt** retorna uma estrutura **FILETIME** que contém a soma dos dois valores inteiros. Os dois parâmetros de entrada permanecem inalterados. Se **pwCarry** for não-nulo, ele contém o resultado deve executar para a soma, 0 ou 1. 
  
## <a name="remarks"></a>Comentários

A função **FtAdcFt** é idêntica ao **FtAddFt** quando _pwCarry_ é NULL. Se _pwCarry_ não for nula e pontos como 0, **FtAdcFt** retorna o mesmo valor **FILETIME** que **FtAddFt** retorna. 
  
## <a name="see-also"></a>Confira também



[FtAddFt](ftaddft.md)

