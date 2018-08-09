---
title: SzFindCh
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SzFindCh
api_type:
- COM
ms.assetid: 3406d060-bfea-4cea-8253-2a9aeb9e8147
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: b517eaffa56001d8c414888ee6cbc8ec4f49cf66
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770566"
---
# <a name="szfindch"></a>SzFindCh
 
**Aplica-se a**: Outlook 
  
Localiza a primeira ocorrência de um caractere em uma cadeia de caracteres terminada em nulo. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Provedores de serviços e aplicativos cliente  <br/> |
   
```cpp
LPSTR SzFindCh(
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

**SzFindCh** retorna um ponteiro para a primeira ocorrência do caractere na cadeia de caracteres. Se o caractere não ocorrer em qualquer lugar na cadeia de caracteres, ou se o parâmetro _lpsz_ é NULL, um valor NULL é retornado. 
  
## <a name="remarks"></a>Comentários

A função **SzFindCh** procura apenas; uma correspondência exata é sensível a maiusculas de minúsculas e diacríticos diferenças. Pesquisas nos formatos Unicode e DBCS são suportadas. 
  

