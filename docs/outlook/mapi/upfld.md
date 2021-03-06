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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431355"
---
# <a name="upfld"></a>UPFLD

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Informações para carregar uma pasta durante o estado [de carregamento da pasta.](upload-folder-state.md)
  
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
  
>  [out]/[in] Sinalizadores para determinar as ações apropriadas para o uplaod. 
    
  - UPF_NEW
    
    - [out] A pasta é nova.
    
  - UPF_MOD_PARENT
    
    - [out] A pasta foi movida.
    
  - UPF_MOD_PROPS
    
    - [out] As propriedades da pasta foram modificadas.
    
  - UPF_DEL
    
    - [out] A pasta foi excluída.
    
  - UPF_OK
    
    - [in] O carregamento foi bem-sucedido. O cliente define isso depois de carregar as informações da pasta no servidor.
    
_pfld_
  
> [out] O objeto de pasta aberta a ser carregado.
    
_feid_
  
> [out] ID da entrada da pasta.
    
## <a name="see-also"></a>Confira também

- [Sobre a API de replicação](about-the-replication-api.md) 
- [Sobre a máquina de estado de replicação](about-the-replication-state-machine.md)
- [Constantes de MAPI](mapi-constants.md)

