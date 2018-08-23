---
title: SzFindLastCh
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SzFindLastCh
api_type:
- COM
ms.assetid: 7c3e5a71-7b78-4328-b8ee-265cc4da4be5
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: eeeff110e5de592d491865079adfa187e5dfa194
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570870"
---
# <a name="szfindlastch"></a>SzFindLastCh

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Procura a última ocorrência de um caractere em uma cadeia de caracteres terminada em nulo. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Provedores de serviços e aplicativos cliente  <br/> |
   
```cpp
LPSTR SzFindLastCh(
  LPCSTR lpsz,
  USHORT ch
);
```

## <a name="parameters"></a>Parâmetros

 _lpsz_
  
> [in] Ponteiro para a cadeia de caracteres terminada em nulo a ser pesquisado. 
    
 _CH_
  
> [in] O caractere a ser pesquisado.
    
## <a name="return-value"></a>Valor retornado

 **SzFindLastCh** retorna um ponteiro para a última ocorrência do caractere na cadeia de caracteres. Se o caractere não ocorrer em qualquer lugar na cadeia de caracteres, ou se o parâmetro _lpsz_ é NULL, um valor NULL é retornado. 
  
## <a name="remarks"></a>Comentários

A função **SzFindLastCh** procura apenas; uma correspondência exata é sensível a maiusculas de minúsculas e diacríticos diferenças. Pesquisas nos formatos Unicode e DBCS são suportadas. 
  

