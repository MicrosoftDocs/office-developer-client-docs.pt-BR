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
ms.openlocfilehash: 7595fac4346a537eed86550432f56a761c27c0ec
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766682"
---
# <a name="getdefcachedmode"></a>GetDefCachedMode

  
  
**Aplica-se a**: Outlook 
  
Indica se o modo cache do Exchange para o armazenamento particular do Exchange está habilitado e, se isso é imposto pela diretiva.
  
## <a name="quick-info"></a>Informações rápidas

|||
|:-----|:-----|
|Exportá-los por:  <br/> |Msmapi32  <br/> |
|Chamado pelo:  <br/> |Cliente  <br/> |
|Implementada por:  <br/> |Outlook  <br/> |
   
```cpp
BOOL GetDefCachedMode(BOOL *pfPolicy); 

```

## <a name="parameters"></a>Parâmetros

 _pfPolicy_
  
> [out] **true** se o valor de retorno é imposto pela diretiva, **false** caso não seja. 
    
## <a name="return-values"></a>Valores de retorno

 **True**
  
- Armazenamento em cache está habilitado.
    
 **False**
  
- O cache é desabilitado.
    
## <a name="see-also"></a>Confira também



[GetDefCachedModeDownloadPubFoldFavs](getdefcachedmodedownloadpubfoldfavs.md)

