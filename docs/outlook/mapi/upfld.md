---
title: UPFLD
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6da9d6b6-a016-ccef-77da-3e037c30450d
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: c8f7bdc5864c049d8db6f38e92a69c97b6f9dc73
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360477"
---
# <a name="upfld"></a>UPFLD

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Informações para carregar uma pasta durante o estado de [pasta de carregamento](upload-folder-state.md).
  
## <a name="quick-info"></a>Informações rápidas

```cpp
struct UPFLD 
{ 
    ULONG ulFlags; 
    LPMAPIFOLDER pfld; 
    FEID feid; 
}; 

```

## <a name="members"></a>Membros

_ulFlags_
  
>  [out]/[in] flags para determinar as ações apropriadas para o uplaod. 
    
  - UPF_NEW
    
    - bota A pasta é nova.
    
  - UPF_MOD_PARENT
    
    - bota A pasta foi movida.
    
  - UPF_MOD_PROPS
    
    - bota As propriedades da pasta foram modificadas.
    
  - UPF_DEL
    
    - bota A pasta foi excluída.
    
  - UPF_OK
    
    - no O upload foi bem-sucedido. O cliente define isso após carregar as informações da pasta no servidor.
    
_pfld_
  
> bota O objeto Folder aberto a ser carregado.
    
_feid_
  
> [out] ID da entrada da pasta.
    
## <a name="see-also"></a>Confira também

- [Sobre a API de replicação](about-the-replication-api.md) 
- [Sobre a máquina de estado de replicação](about-the-replication-state-machine.md)
- [Constantes de MAPI](mapi-constants.md)

