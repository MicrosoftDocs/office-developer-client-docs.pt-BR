---
title: DNHIER
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3953dc9d-0146-3689-63f0-c6ba78566b8b
description: 'Última modificação: 05 de julho de 2012'
ms.openlocfilehash: 06f30b4856fc10127aec99975652e28a5e8dda30
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389082"
---
# <a name="dnhier"></a>DNHIER

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Informações para baixar uma hierarquia do servidor durante o [estado hierarquia de download](download-hierarchy-state.md), que é parte de uma sincronização de hierarquia completa. Este processo de download usa a sincronização de Sincronização de Alteração Incremental (ICS) do Microsoft Exchange. Confira mais informações sobre ICS em [Critérios de avaliação de ICS](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).
  
## <a name="quick-info"></a>Informações rápidas

```cpp
struct DNHIER 
{ 
    ULONG ulFlags; 
    LPSTREAM pstmReserved; 
    PXIHC pxihc; 
    UINT cEntNew; 
   UINT cEntMod; 
    UINT cEntDel; 
};
```

## <a name="members"></a>Membros

_ulFlags_
  
>  [in] Sinaliza para determinar o comportamento apropriado durante o download. 
    
   - DNH_OK
    
   - [in] Download bem-sucedido. O cliente define isso depois de baixar informações do servidor.
    
_pstmReserved_
  
> [uto] Esse membro é reservado para uso interno do Outlook e não tem suporte. 
    
_pxihc_
  
>  [uto] Ponteiro para a hierarquia de hierarquia **IExchangeImportHierarchyChanges** que suporta o download de alterações incrementais de hierarquia. Para saber mais sobre **IExchangeImportHierarchyChanges**, confira [Critérios de avaliação de ICS](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).
    
_cEntNew_
  
> [out] Número de pastas adicionadas ao repositório local. O Outlook preenche esse valor durante o download ao usar a ICS.
    
_cEntMod_
  
> [out] Número de pastas a serem modificadas no repositório local. O Outlook preenche esse valor durante o download ao usar a ICS.
    
_cEntDel_
  
> [out] Número de pastas a serem excluídas do repositório local. O Outlook preenche esse valor durante o download ao usar a ICS.
    
## <a name="see-also"></a>Confira também

- [Sobre a máquina de estado de replicação](about-the-replication-state-machine.md) 
- [Constantes de MAPI](mapi-constants.md)

