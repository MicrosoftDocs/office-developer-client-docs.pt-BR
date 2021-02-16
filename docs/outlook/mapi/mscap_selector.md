---
title: MSCAP_SELECTOR
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f28ac144-f5ac-fd83-2b72-8d6e5fd74b6e
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 9c5d8ab5bbac91250f3b8c552ad891c62134526e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417200"
---
# <a name="mscap_selector"></a>MSCAP_SELECTOR

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Especifica os recursos a retornar para um armazenamento.
  
## <a name="quick-info"></a>Informações rápidas

```cpp
typedef enum 
{ 
    MSCAP_SEL_RESERVED1 = 0, 
    MSCAP_SEL_RESERVED2, 
    MSCAP_SEL_FOLDER, 
    MSCAP_SEL_RESERVED3, 
    MSCAP_SEL_RESTRICTION, 
} MSCAP_SELECTOR;
```

## <a name="members"></a>Membros

 *MSCAP_SEL_RESERVED1* 
  
> Este membro está reservado para uso interno do Outlook e não tem suporte. 
    
 *MSCAP_SEL_RESERVED2* 
  
> Este membro é reservado para uso interno do Outlook e não tem suporte. 
    
 *MSCAP_SEL_FOLDER* 
  
> Recursos sobre suporte a pastas em um armazenamento.
    
 *MSCAP_SEL_RESERVED3* 
  
> Este membro é reservado para uso interno do Outlook e não tem suporte. 
    
 *MSCAP_SEL_RESTRICTION* 
  
> Recursos sobre o suporte a restrições em um armazenamento.
    

