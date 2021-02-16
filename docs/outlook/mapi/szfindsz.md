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
ms.openlocfilehash: 9fc21a27cb6c9041bdd8976ce5f030f0ab9eb57f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435219"
---
# <a name="szfindsz"></a>SzFindSz

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Localiza a primeira ocorrência de uma substring terminada por caractere nulo em uma cadeia de caracteres terminada por caractere nulo. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos cliente e provedores de serviços  <br/> |
   
```cpp
LPSTR SzFindCh(
  LPCSTR lpsz,
  LPCSTR lpszKey
);
```

## <a name="parameters"></a>Parâmetros

 _lpsz_
  
> [in] Ponteiro para a cadeia de caracteres terminada por nulo a ser pesquisada. O  _parâmetro lpsz_ não deve exceder 65536 caracteres. 
    
 _lpszKey_
  
> [in] Ponteiro para a substring terminada por nulo a ser pesquisada. O  _parâmetro lpszKey_ não deve exceder 65536 caracteres. 
    
## <a name="return-value"></a>Valor de retorno

 **SzFindSz** retorna um ponteiro para o primeiro caractere da primeira ocorrência da substring na cadeia de caracteres. Se a substring não ocorrer em qualquer lugar na cadeia de  _caracteres, se lpszKey_ for maior que  _lpsz_ ou se um dos parâmetros for NULL, um valor null será retornado. 
  
## <a name="remarks"></a>Comentários

A **função SzFindSz** procura apenas uma combinação exata; é sensível a diferenças de caso e diacrítico. Há suporte para pesquisas nos formatos Unicode e DBCS. O limite de comprimento em ambos os parâmetros está em caracteres, não necessariamente bytes. 
  

