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
ms.openlocfilehash: 522c67b19656c00ea169def98a42ca2b3c1db840
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345238"
---
# <a name="szfindch"></a>SzFindCh
 
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Procura a primeira ocorrência de um caractere em uma cadeia de caracteres terminada em nulo. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs. h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos cliente e provedores de serviços  <br/> |
   
```cpp
LPSTR SzFindCh(
  LPCSTR lpsz,
  USHORT ch
);
```

## <a name="parameters"></a>Parâmetros

_lpsz_
  
> no Ponteiro para a cadeia de caracteres terminada em nulo a ser pesquisada. 
    
_CA_
  
> no O caractere a ser procurado.
    
## <a name="return-value"></a>Valor de retorno

**SzFindCh** retorna um ponteiro para a primeira ocorrência do caractere na cadeia de caracteres. Se o caractere não ocorrer em qualquer lugar na cadeia de caracteres ou se o parâmetro _lpsz_ for NULL, um valor NULL será retornado. 
  
## <a name="remarks"></a>Comentários

A função **SzFindCh** pesquisa apenas uma correspondência exata; é sensível às diferenças de maiúsculas e minúsculas. As pesquisas nos formatos Unicode e DBCS são suportadas. 
  

