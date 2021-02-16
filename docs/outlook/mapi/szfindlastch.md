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
ms.openlocfilehash: f22d30c1bc7c797834f58bcd1306b14ac2542c6d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421253"
---
# <a name="szfindlastch"></a>SzFindLastCh

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Procura a última ocorrência de um caractere em uma cadeia de caracteres terminada em nulo. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos cliente e provedores de serviços  <br/> |
   
```cpp
LPSTR SzFindLastCh(
  LPCSTR lpsz,
  USHORT ch
);
```

## <a name="parameters"></a>Parâmetros

 _lpsz_
  
> [in] Ponteiro para a cadeia de caracteres terminada em nulo a ser pesquisada. 
    
 _ch_
  
> [in] O caractere a ser pesquisado.
    
## <a name="return-value"></a>Valor de retorno

 **SzFindLastCh** retorna um ponteiro para a última ocorrência do caractere na cadeia de caracteres. Se o caractere não ocorrer em qualquer lugar na cadeia de caracteres ou se o parâmetro  _lpsz_ for NULL, um valor null será retornado. 
  
## <a name="remarks"></a>Comentários

A **função SzFindLastCh** procura apenas uma combinação exata; é sensível a diferenças de caso e diacrítico. Há suporte para pesquisas nos formatos Unicode e DBCS. 
  

