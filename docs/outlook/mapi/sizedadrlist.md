---
title: SizedADRLIST
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedADRLIST
api_type:
- COM
ms.assetid: 5c64d74a-83a7-4122-b1d1-fcca0f4a6cdb
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 62911e0dec15002f39fff81e8c517c1cb11d0183
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574738"
---
# <a name="sizedadrlist"></a>SizedADRLIST

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Define uma estrutura [ADRLIST](adrlist.md) com o nome especificado que contém um número especificado de estruturas [ADRENTRY](adrentry.md) . 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
|Estrutura relacionada:  <br/> |**ADRLIST** <br/> |
   
```cpp
SizedADRLIST (_centries,_name)
```

## <a name="parameters"></a>Parâmetros

__centries_
  
> Contagem de estruturas **ADRENTRY** a serem incluídos na nova estrutura **ADRLIST** . 
    
__nome_
  
> Nome para a nova estrutura **ADRLIST** . 
    
## <a name="remarks"></a>Comentários

A macro **SizedADRLIST** permite definir uma lista de destinatários que possui limites explícitos quando os requisitos de tamanho da matriz são conhecidos. O código a seguir mostra como orientar o resultado da macro **SizedADRLIST** para um ponteiro de estrutura **ADRLIST** : 
  
```cpp
lpADRList = (LPADRLIST) &SizedADRList;
```

## <a name="see-also"></a>Confira também

- [ADRLIST](adrlist.md)
- [ADRENTRY](adrentry.md)
- [Macros relacionadas a estruturas](macros-related-to-structures.md)

