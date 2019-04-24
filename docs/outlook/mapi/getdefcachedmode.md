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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299703"
---
# <a name="getdefcachedmode"></a>GetDefCachedMode

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Indica se o modo cache do Exchange para o repositório particular do Exchange está habilitado e se ele é imposto pela política.
  
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
  
> bota **true** se o valor de retorno é imposto por política, **false** se não for. 
    
## <a name="return-values"></a>Valor de retorno

 **verdadeiro**
  
- O cache está habilitado.
    
 **false**
  
- O armazenamento em cache está desabilitado.
    
## <a name="see-also"></a>Confira também



[GetDefCachedModeDownloadPubFoldFavs](getdefcachedmodedownloadpubfoldfavs.md)

