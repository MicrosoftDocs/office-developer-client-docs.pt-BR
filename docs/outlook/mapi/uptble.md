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
ms.openlocfilehash: b2523c149d98dacf9ad321a4a443382a39753fd5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592336"
---
# <a name="uptble"></a>UPTBLE

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Informações para carregar o conteúdo de uma pasta durante o [estado da tabela de carregar](upload-table-state.md)estendidas.
  
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

## <a name="members"></a>Members

 _iEntMod_
  
>  [out] Índice para controlar o carregamento _cEntMod_ número de itens de novos ou modificados. 
    
 _cEntMod_
  
>  [out] Número de itens de novos ou modificados na pasta. 
    
 _iEntRead_
  
>  [out] Índice para acompanhar carregando o número de _cEntRead_ ler itens. 
    
 _cEntRead_
  
>  [out] Número de itens de leitura na pasta. 
    
 _iEntDel_
  
>  [out] Itens excluídos do índice para rastrear carregando o número de _cEntDel_ . 
    
 _cEntDel_
  
>  [out] Número de itens excluídos na pasta. 
    
## <a name="see-also"></a>Confira também

- [Sobre a API de replicação](about-the-replication-api.md) 
- [Sobre a máquina de estado de replicação](about-the-replication-state-machine.md)
- [UPTBL](uptbl.md)

