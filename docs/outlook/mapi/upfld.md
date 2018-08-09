---
title: UPFLD
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6da9d6b6-a016-ccef-77da-3e037c30450d
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: f25b3fb967f4ed93ac38487f21145f35413764da
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770668"
---
# <a name="upfld"></a>UPFLD

**Aplica-se a**: Outlook 
  
Informações de carregamento de uma pasta durante o [carregamento do estado da pasta](upload-folder-state.md).
  
## <a name="quick-info"></a>Informações rápidas

```cpp
struct UPFLD 
{ 
    ULONG ulFlags; 
    LPMAPIFOLDER pfld; 
    FEID feid; 
}; 

```

## <a name="members"></a>Members

_ulFlags_
  
>  [out] / [in] sinalizadores para determinar as ações apropriadas para a uplaod. 
    
  - UPF_NEW
    
    - [out] Pasta é nova.
    
  - UPF_MOD_PARENT
    
    - [out] Pasta foi movida.
    
  - UPF_MOD_PROPS
    
    - [out] Propriedades da pasta foram modificadas.
    
  - UPF_DEL
    
    - [out] Pasta foi excluída.
    
  - UPF_OK
    
    - [in] Carregamento foi bem-sucedida. O cliente define esta após carregar as informações da pasta no servidor.
    
_pfld_
  
> [out] O objeto de pasta aberta para carregar.
    
_feid_
  
> [out] Identificação de entrada da pasta.
    
## <a name="see-also"></a>Confira também

- [Sobre a API de replicação](about-the-replication-api.md) 
- [Sobre a máquina de estado de replicação](about-the-replication-state-machine.md)
- [Constantes MAPI](mapi-constants.md)

