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
ms.openlocfilehash: c35a1eb54b29c04bc8eed453272b59aae0ea737e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423458"
---
# <a name="sizedadrlist"></a>SizedADRLIST

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Define uma estrutura [das ADRLIST](adrlist.md) com o nome especificado que contém um número especificado de estruturas [ADRENTRY](adrentry.md) . 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs. h  <br/> |
|Estrutura relacionada:  <br/> |**ADRLIST** <br/> |
   
```cpp
SizedADRLIST (_centries,_name)
```

## <a name="parameters"></a>Parâmetros

__cEntries_
  
> Contagem de estruturas **ADRENTRY** a serem incluídas na nova estrutura **das ADRLIST** . 
    
__nome_
  
> Nome para a nova estrutura **das ADRLIST** . 
    
## <a name="remarks"></a>Comentários

A macro **SizedADRLIST** permite definir uma lista de destinatários que tenha limites explícitos quando os requisitos de comprimento de matriz forem conhecidos. O código a seguir mostra como converter o resultado da macro **SizedADRLIST** para um ponteiro de estrutura **das ADRLIST** : 
  
```cpp
lpADRList = (LPADRLIST) &SizedADRList;
```

## <a name="see-also"></a>Confira também

- [ADRLIST](adrlist.md)
- [ADRENTRY](adrentry.md)
- [Macros relacionadas a estruturas](macros-related-to-structures.md)

