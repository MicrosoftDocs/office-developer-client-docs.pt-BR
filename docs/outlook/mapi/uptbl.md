---
title: UPTBL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 39d9ad3b-ff4b-8378-a3ac-d5621c7ef7f1
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: b401f54df020fb6553cbdcc5b85206ee422a8429
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438110"
---
# <a name="uptbl"></a>UPTBL

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Informações para carregar o conteúdo de uma pasta durante o estado [da tabela de carregamento.](upload-table-state.md)
  
## <a name="quick-info"></a>Informações rápidas

```cpp
struct UPTBL 
{ 
    ULONG ulFlags; 
    LPSTREAM pstmReserved; 
    LPSTR pszName; 
    FEID feid; 
    UINT uintReserved; 
    UPTBLE rgte[2]; 
    UINT iEnt; 
    UINT cEnt; 
    PUPMOV pupmovHead; 
    void* pReserved; 
};
```

## <a name="members"></a>Membros

_ulFlags_
  
> [in] Sinalizadores para determinar o comportamento apropriado durante o carregamento.
    
  - UPT_OK
    
    - [in] O carregamento foi bem-sucedido. O cliente define isso depois de carregar o conteúdo da pasta no servidor.
    
_pstmReserved_
  
> [uto] Esse membro é reservado para uso interno do Outlook e não tem suporte. 
    
_pszName_
  
> [out] Nome da pasta.
    
_feid_
  
> [out] ID da entrada da pasta.
    
_uintReserved_
  
> [out] Esse membro é reservado para uso interno do Outlook e não tem suporte. 
    
_rgte_
  
> [out] Estrutura para manter as seguintes informações para itens normais (ou não ocultos) e itens associados (ou ocultos) na pasta:  _rgte[0]_ é para itens normais e  _rgte[1]_ é para itens associados. 
    
   - o número de itens novos ou modificados
   - o número de itens lidos 
   - o número de itens excluídos
    
 _iEnt_
  
> [out] Index to track uploading the number of changes specified by  _cEnt_.
    
_cEnt_
  
> [out] Número de alterações na pasta.
    
_entremovHead_
  
> [out] Cadeia de [estruturas UPMOV.](upmov.md) 
    
_pReserved_
  
> [out] Esse membro é reservado para uso interno do Outlook e não tem suporte.
    
## <a name="see-also"></a>Confira também

- [Sobre a API de replicação](about-the-replication-api.md)
- [Sobre a máquina de estado de replicação](about-the-replication-state-machine.md)
- [Constantes de MAPI](mapi-constants.md)
- [UPTBLE](uptble.md)

