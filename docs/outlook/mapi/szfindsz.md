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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345742"
---
# <a name="szfindsz"></a>SzFindSz

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Localiza a primeira ocorrência de uma subcadeia de caracteres terminada em nulo em uma cadeia de caracteres terminada em nulo. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil. h  <br/> |
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
  
> no Ponteiro para a cadeia de caracteres terminada em nulo a ser pesquisada. O parâmetro _lpsz_ não deve exceder 65536 caracteres. 
    
 _lpszKey_
  
> no Ponteiro para a subcadeia de caracteres terminada em nulo a ser pesquisada. O parâmetro _lpszKey_ não deve exceder 65536 caracteres. 
    
## <a name="return-value"></a>Valor de retorno

 **SzFindSz** retorna um ponteiro para o primeiro caractere da primeira ocorrência da subcadeia de caracteres na cadeia de caracteres. Se a subcadeia de caracteres não ocorrer em qualquer lugar na cadeia de caracteres, se _lpszKey_ for maior do que _lpsz_, ou se um dos parâmetros for NULL, um valor NULL será retornado. 
  
## <a name="remarks"></a>Comentários

A função **SzFindSz** pesquisa apenas uma correspondência exata; é sensível às diferenças de maiúsculas e minúsculas. Pesquisas em formatos Unicode e DBCS são suportadas. O limite de tamanho em ambos os parâmetros é em caracteres, não necessariamente em bytes. 
  

