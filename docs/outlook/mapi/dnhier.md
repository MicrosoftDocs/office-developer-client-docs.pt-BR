---
title: DNHIER
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3953dc9d-0146-3689-63f0-c6ba78566b8b
description: '�ltima altera��o: quinta-feira, 5 de julho de 2012'
ms.openlocfilehash: fbf064201bf8d2733c3eea1e1a24f77b146a23c9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564567"
---
# <a name="dnhier"></a>DNHIER

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Informações para download de uma hierarquia do servidor durante o [estado de hierarquia de download](download-hierarchy-state.md), que é parte de uma sincronização de hierarquia completa. Este processo de download usa a sincronização de alteração Incremental do Microsoft Exchange (ICS). Para obter mais informações sobre ICS, consulte [ICS critérios de avaliação](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx).
  
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

## <a name="members"></a>Members

_ulFlags_
  
>  [in] Sinalizadores para determinar o comportamento apropriado durante o download. 
    
   - DNH_OK
    
   - [in] Download teve êxito. O cliente define esta após fazer o download de informações do servidor.
    
_pstmReserved_
  
> [out] Este membro é reservado para uso interno do Outlook e não é suportado. 
    
_pxihc_
  
>  [out] Ponteiro para a interface de hierarquia de **IExchangeImportHierarchyChanges** que suporta o download de alterações incrementais de hierarquia. Para obter mais informações sobre **IExchangeImportHierarchyChanges**, consulte [ICS critérios de avaliação](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx).
    
_cEntNew_
  
> [out] Número de pastas adicionados ao armazenamento local. Outlook preenche esse valor durante o download quando usando ICS.
    
_cEntMod_
  
> [out] Número de pastas a serem modificadas no repositório local. Outlook preenche esse valor durante o download quando usando ICS.
    
_cEntDel_
  
> [out] Número de pastas a ser excluído no armazenamento local. Outlook preenche esse valor durante o download quando usando ICS.
    
## <a name="see-also"></a>Confira também

- [Sobre a máquina de estado de replicação](about-the-replication-state-machine.md) 
- [Constantes MAPI](mapi-constants.md)

