---
title: GetDefCachedModeDownloadPubFoldFavs
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2dd95561-ed8f-8a3b-6532-b53556f16666
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 5e623c9d40ffd2dd276bd9601676244644bb3402
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299885"
---
# <a name="getdefcachedmodedownloadpubfoldfavs"></a>GetDefCachedModeDownloadPubFoldFavs

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Indica se o modo cache do Exchange para a pasta **favoritos da pasta pública** está habilitado e se isso é imposto pela política. 
  
## <a name="quick-info"></a>Informações rápidas

|||
|:-----|:-----|
|Exportado por:  <br/> |msmapi32.dll  <br/> |
|Chamado por:  <br/> |Cliente  <br/> |
|Implementado por:  <br/> |Outlook  <br/> |
   
```cpp
BOOL GetDefCachedModeDownloadPubFoldFavs(BOOL *pfPolicy); 

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



[GetDefCachedMode](getdefcachedmode.md)

