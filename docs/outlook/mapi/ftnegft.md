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
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: db208dad8697060e394b3ee037ea658cefbab669
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423381"
---
# <a name="ftnegft"></a>FtNegFt

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Computa o complemento de um inteiro de 64 bits não assinado. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil. h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos cliente e provedores de serviços  <br/> |
   
```cpp
FILETIME FtNegFt(
  FILETIME ft
);
```

## <a name="parameters"></a>Parâmetros

 _ft_
  
> no Uma estrutura [FILETIME](filetime.md) que contém o inteiro de 64 bits não assinado para o qual calcular o complemento de dois. 
    
## <a name="return-value"></a>Valor de retorno

A função **FtNegFt** retorna uma estrutura **FILETIME** que contém o complemento de dois do inteiro. O parâmetro de entrada permanecerá inalterado. 
  

