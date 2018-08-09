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
ms.openlocfilehash: c221f98d6551ea63971dd378d522c1f2bebb312b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770568"
---
# <a name="szfindlastch"></a>SzFindLastCh

  
  
**Aplica-se a**: Outlook 
  
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
  

