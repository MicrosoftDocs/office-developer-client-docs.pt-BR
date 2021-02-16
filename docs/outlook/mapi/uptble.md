---
title: UPTBLE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f7fcb385-186d-d5fe-7104-fe0af09d5768
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: d0b440f01aad7078ed76cd37d36c5ad506215438
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413837"
---
# <a name="uptble"></a>UPTBLE

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Informações estendidas para carregar o conteúdo de uma pasta durante o [estado da tabela de carregamento.](upload-table-state.md)
  
## <a name="quick-info"></a>Informações rápidas

```cpp
struct UPTBLE 
{ 
    UINTiEntMod; 
    UINTcEntMod; 
    UINTiEntRead; 
    UINTcEntRead; 
    UINTiEntDel; 
    UINTcEntDel; 
};
```

## <a name="members"></a>Membros

 _iEntMod_
  
>  [out] Index to tracking the  _cEntMod_ number of new or modified items. 
    
 _cEntMod_
  
>  [out] Número de itens novos ou modificados na pasta. 
    
 _iEntRead_
  
>  [out] Index to track uploading the number of  _cEntRead_ read items. 
    
 _cEntRead_
  
>  [out] Número de itens de leitura na pasta. 
    
 _iEntDel_
  
>  [out] Index to track uploading the number of  _cEntDel_ deleted items. 
    
 _cEntDel_
  
>  [out] Número de itens excluídos na pasta. 
    
## <a name="see-also"></a>Confira também

- [Sobre a API de replicação](about-the-replication-api.md) 
- [Sobre a máquina de estado de replicação](about-the-replication-state-machine.md)
- [UPTBL](uptbl.md)

