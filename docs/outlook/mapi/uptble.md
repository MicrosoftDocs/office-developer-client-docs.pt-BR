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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329705"
---
# <a name="uptble"></a>UPTBLE

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Informações estendidas para carregar o conteúdo de uma pasta durante o [estado de carregamento da tabela](upload-table-state.md).
  
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
  
>  bota Index para acompanhar o carregamento do número _cEntMod_ de itens novos ou modificados. 
    
 _cEntMod_
  
>  bota Número de itens novos ou modificados na pasta. 
    
 _iEntRead_
  
>  bota Index para acompanhar o carregamento do número de itens de leitura _cEntRead_ . 
    
 _cEntRead_
  
>  bota Número de itens lidos na pasta. 
    
 _iEntDel_
  
>  bota Index para acompanhar o carregamento do número de itens excluídos do _cEntDel_ . 
    
 _cEntDel_
  
>  bota Número de itens excluídos na pasta. 
    
## <a name="see-also"></a>Confira também

- [Sobre a API de replicação](about-the-replication-api.md) 
- [Sobre a máquina de estado de replicação](about-the-replication-state-machine.md)
- [UPTBL](uptbl.md)

