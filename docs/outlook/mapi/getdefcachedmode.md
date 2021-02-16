---
title: GetDefCachedMode
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 325b6b47-b6a6-503e-e9bb-65ef7b73d659
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 8e8a6ac07e14af52337b6e280fa58274df453c65
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412741"
---
# <a name="getdefcachedmode"></a>GetDefCachedMode

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Indica se o Modo Cache do Exchange para o armazenamento particular do Exchange está habilitado e se isso é imposto pela política.
  
## <a name="quick-info"></a>Informações rápidas

|||
|:-----|:-----|
|Exportado por:  <br/> |msmapi32.dll  <br/> |
|Chamado por:  <br/> |Cliente  <br/> |
|Implementado por:  <br/> |Outlook  <br/> |
   
```cpp
BOOL GetDefCachedMode(BOOL *pfPolicy); 

```

## <a name="parameters"></a>Parâmetros

 _pfPolicy_
  
> [out] **true** se o valor de retorno for imposto pela política, **false** se não for. 
    
## <a name="return-values"></a>Valor de retorno

 **verdadeiro**
  
- O cache está habilitado.
    
 **falso**
  
- O cache está desabilitado.
    
## <a name="see-also"></a>Confira também



[GetDefCachedModeDownloadPubFoldFavs](getdefcachedmodedownloadpubfoldfavs.md)

