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
ms.openlocfilehash: ad561bd3be7fd0c9f25c11875f62667563dfcbe7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578259"
---
# <a name="ftsubft"></a>FtSubFt

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
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

## <a name="parameters"></a>Parâmetros

 _Minuend_
  
> [in] Uma estrutura [FILETIME](filetime.md) que contém o inteiro não assinado de 64 bits do qual o valor no parâmetro _Subtrahend_ deve ser subtraídos. 
    
 _Subtrahend_
  
> [in] Uma estrutura **FILETIME** que contém o inteiro não assinado de 64 bits é subtraído do valor indicado pelo parâmetro _Minuend_ . 
    
## <a name="return-value"></a>Valor retornado

A função **FtSubFt** retorna uma estrutura **FILETIME** que contém o resultado de subtração. Os dois parâmetros de entrada permanecem inalterados. 
  

