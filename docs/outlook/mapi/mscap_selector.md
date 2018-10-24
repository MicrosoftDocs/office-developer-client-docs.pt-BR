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
ms.openlocfilehash: 8c23788d64fe3703c7c46998cade0bd40d2f3dd2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588122"
---
# <a name="mscapselector"></a>MSCAP_SELECTOR

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Especifica os recursos para retornar para um repositório.
  
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

## <a name="members"></a>Members

 *MSCAP_SEL_RESERVED1* 
  
> Este membro é reservado para uso interno do Outlook e não é suportado. 
    
 *MSCAP_SEL_RESERVED2* 
  
> Este membro é reservado para uso interno do Outlook e não é suportado. 
    
 *MSCAP_SEL_FOLDER* 
  
> Recursos sobre o suporte a pastas em um repositório.
    
 *MSCAP_SEL_RESERVED3* 
  
> Este membro é reservado para uso interno do Outlook e não é suportado. 
    
 *MSCAP_SEL_RESTRICTION* 
  
> Recursos sobre o suporte a restrições em um repositório.
    

