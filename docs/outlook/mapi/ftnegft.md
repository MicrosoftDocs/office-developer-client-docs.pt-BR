---
title: FtNegFt
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FtNegFt
api_type:
- COM
ms.assetid: 639a408c-aed1-456b-9f75-9d6fb8dcb33b
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: e26acb8415df007a7f3fb5901521da7222ae40ed
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766643"
---
# <a name="ftnegft"></a>FtNegFt

  
  
**Aplica-se a**: Outlook 
  
Computa das duas complemento de um inteiro não assinado de 64 bits. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil.h  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Provedores de serviços e aplicativos cliente  <br/> |
   
```cpp
FILETIME FtNegFt(
  FILETIME ft
);
```

## <a name="parameters"></a>Par�metros

 _FT_
  
> [in] Uma estrutura [FILETIME](filetime.md) que contém o inteiro não assinado de 64 bits para a qual calcular das duas complemento. 
    
## <a name="return-value"></a>Valor retornado

A função **FtNegFt** retorna uma estrutura **FILETIME** que contém das duas complemento do inteiro. O parâmetro de entrada permanecerá inalterado. 
  

