---
title: DNTBLE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 10fb1650-6c3e-f467-91cd-48e5ddd82827
description: '�ltima altera��o: quinta-feira, 5 de julho de 2012'
ms.openlocfilehash: 51a79075dac62a051f5a28dbcb70e7d6ff200e65
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766487"
---
# <a name="dntble"></a>DNTBLE

  
  
**Aplica-se a**: Outlook 
  
Informações para baixar o conteúdo de uma pasta do servidor durante a [baixar o estado da tabela](download-table-state.md). Este processo de download usa a sincronização de alteração Incremental do Microsoft Exchange (ICS). Para obter mais informações sobre ICS, consulte [ICS critérios de avaliação](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx).
  
## <a name="quick-info"></a>Informações rápidas

```cpp
struct DNTBLE 
{ 
    UINT cEntNew; 
    UINT cEntMod; 
    UINT cEntRead; 
    UINT cEntDel; 
};
```

## <a name="members"></a>Membros

 _cEntNew_
  
> [out] Número de itens adicionados ao armazenamento local. Outlook preenche esse valor durante o download quando usando ICS.
    
 _cEntMod_
  
> [out] Número de itens modificados no mesmo armazenamento local. Outlook preenche esse valor durante o download quando usando ICS.
    
 _cEntRead_
  
> [out] Número de itens de leitura ou marcado como não lido no armazenamento local. Outlook preenche esse valor durante o download quando usando ICS.
    
 _cEntDel_
  
> [out] Número de itens excluídos no repositório local. Outlook preenche esse valor durante o download quando usando ICS.
    
## <a name="see-also"></a>Confira também



[Sobre a máquina de estado de replicação](about-the-replication-state-machine.md)
  
[Constantes MAPI](mapi-constants.md)
  
[DNTBL](dntbl.md)

