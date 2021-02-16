---
title: FtSubFt
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FtSubFt
api_type:
- COM
ms.assetid: 6619fc41-5518-44ce-85c1-6b0077ed5cb9
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: edd789a586adc71289ff821aa7cf7a33f79fb738
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408415"
---
# <a name="ftsubft"></a>FtSubFt

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Subtrai um inteiro de 64 bits não assinado de outro. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos cliente e provedores de serviços  <br/> |
   
```cpp
FILETIME FtSubFt(
  FILETIME Minuend,
  FILETIME Subtrahend
);
```

## <a name="parameters"></a>Parâmetros

 _Minuend_
  
> [in] Uma [estrutura FILETIME](filetime.md) que contém o inteiro de 64 bits não assinado do qual o valor no parâmetro  _Subtrahend_ deve ser subtraído. 
    
 _Subtrahend_
  
> [in] Uma **estrutura FILETIME** que contém o inteiro de 64 bits não assinado que é subtraído do valor indicado pelo parâmetro _Minuend._ 
    
## <a name="return-value"></a>Valor de retorno

A **função FtSubFt** retorna uma **estrutura FILETIME** que contém o resultado da subtração. Os dois parâmetros de entrada permanecem inalterados. 
  

