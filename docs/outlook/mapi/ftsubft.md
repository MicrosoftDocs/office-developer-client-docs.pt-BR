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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 954630b0b92772d961dc61084c28a9ab419e4c2f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766638"
---
# <a name="ftsubft"></a>FtSubFt

  
  
**Aplica-se a**: Outlook 
  
Subtrai um inteiro não assinado de 64 bits do outro. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil.h  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Provedores de serviços e aplicativos cliente  <br/> |
   
```cpp
FILETIME FtSubFt(
  FILETIME Minuend,
  FILETIME Subtrahend
);
```

## <a name="parameters"></a>Par�metros

 _Minuend_
  
> [in] Uma estrutura [FILETIME](filetime.md) que contém o inteiro não assinado de 64 bits do qual o valor no parâmetro _Subtrahend_ deve ser subtraídos. 
    
 _Subtrahend_
  
> [in] Uma estrutura **FILETIME** que contém o inteiro não assinado de 64 bits é subtraído do valor indicado pelo parâmetro _Minuend_ . 
    
## <a name="return-value"></a>Valor retornado

A função **FtSubFt** retorna uma estrutura **FILETIME** que contém o resultado de subtração. Os dois parâmetros de entrada permanecem inalterados. 
  

