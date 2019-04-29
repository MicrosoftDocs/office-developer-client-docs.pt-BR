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
ms.openlocfilehash: f308c1f6f3cd2c9904dd94cd6761517bd5b410b6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429702"
---
# <a name="ftadcft"></a>FtAdcFt

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Adiciona um inteiro de 64 bits não assinado a outro, opcionalmente usando um sinalizador de transporte.
  
|||
|:-----|:-----|
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos cliente e provedores de serviços  <br/> |
   
```cpp
FILETIME FtAdcFt( 
  FILETIME ft1, 
  FILETIME ft2, 
  WORD FAR *pwCarry
);
```

## <a name="parameters"></a>Parâmetros

 _FT1_
  
> no Uma estrutura [FILETIME](filetime.md) que contém o primeiro inteiro de 64 bits não assinado a ser adicionado. 
    
 _ft2_
  
> no Uma estrutura FILETIME que contém o segundo inteiro não assinado de 64 bits a ser adicionado.
    
 _pwCarry_
  
> [in, out, optional] Na entrada, um ponteiro para o sinalizador transporte de entrada. Na saída, um ponteiro para o resultado de transporte para a adição. Esse parâmetro pode ser NULL se o resultado de transporte não for necessário.
    
## <a name="return-value"></a>Valor de retorno

A função **FtAdcFt** retorna uma estrutura **FILETIME** que contém a soma dos dois inteiros. Os dois parâmetros de entrada permanecem inalterados. Se **pwCarry** for não nulo, ele conterá o resultado de transporte da soma, 0 ou 1. 
  
## <a name="remarks"></a>Comentários

A função **FtAdcFt** é idêntica a **FtAddFt** quando _pwCarry_ é nulo. Se _pwCarry_ não for nulo e apontar para 0, **FtAdcFt** retornará o mesmo valor **FILETIME** que **FtAddFt** retorna. 
  
## <a name="see-also"></a>Confira também



[FtAddFt](ftaddft.md)

