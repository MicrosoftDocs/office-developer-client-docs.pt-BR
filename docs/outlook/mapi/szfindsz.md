---
title: SzFindSz
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SzFindSz
api_type:
- COM
ms.assetid: f4584569-1246-4ac9-a404-48284e4920d7
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 0cc8f25271d1494ebdaca82caa2e77839f299276
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770570"
---
# <a name="szfindsz"></a>SzFindSz

  
  
**Aplica-se a**: Outlook 
  
Localiza a primeira ocorrência de uma subcadeia de caracteres terminada em nulo em uma cadeia de caracteres terminada em nulo. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil.h  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Provedores de serviços e aplicativos cliente  <br/> |
   
```cpp
LPSTR SzFindCh(
  LPCSTR lpsz,
  LPCSTR lpszKey
);
```

## <a name="parameters"></a>Parâmetros

 _lpsz_
  
> [in] Ponteiro para a cadeia de caracteres terminada em nulo a ser pesquisado. O parâmetro _lpsz_ não deve exceder 65.536 caracteres. 
    
 _lpszKey_
  
> [in] Ponteiro para a subcadeia de caracteres terminada em nulo a ser pesquisado. O parâmetro _lpszKey_ não deve exceder 65.536 caracteres. 
    
## <a name="return-value"></a>Valor retornado

 **SzFindSz** retorna um ponteiro para o primeiro caractere da primeira ocorrência da subcadeia de caracteres na cadeia de caracteres. Se a subcadeia de caracteres não ocorrer em qualquer lugar na cadeia de caracteres, se _lpszKey_ for maior do que _lpsz_, ou se o parâmetro for NULL, um valor NULL será retornado. 
  
## <a name="remarks"></a>Comentários

A função **SzFindSz** procura apenas; uma correspondência exata é sensível a maiusculas de minúsculas e diacríticos diferenças. Pesquisas nos formatos Unicode e DBCS são suportadas. O limite de tamanho em ambos os parâmetros é em caracteres, não necessariamente bytes. 
  

