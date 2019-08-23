---
title: DNTBLE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 10fb1650-6c3e-f467-91cd-48e5ddd82827
description: 'Última modificação: 05 de julho de 2012'
ms.openlocfilehash: 41a61bd05bd511888aeab756166016813f4dceb8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337111"
---
# <a name="dntble"></a>DNTBLE

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Informações para baixar o conteúdo de uma pasta do servidor durante o [estado de download de tabela](download-table-state.md). Este processo de download usa a sincronização de Sincronização de Alteração Incremental (ICS) do Microsoft Exchange. Confira mais informações sobre ICS em [Critérios de avaliação de ICS](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).
  
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
  
> [out] Número de itens adicionados ao repositório local. O Outlook preenche esse valor durante o download ao usar ICS.
    
 _cEntMod_
  
> [out] Número de itens modificados no repositório local. O Outlook preenche esse valor durante o download ao usar ICS.
    
 _cEntRead_
  
> [out] Número de itens lidos ou marcados como não lidos no repositório local. O Outlook preenche esse valor durante o download ao usar ICS.
    
 _cEntDel_
  
> [out] Número de itens excluídos do repositório local. O Outlook preenche esse valor durante o download ao usar ICS.
    
## <a name="see-also"></a>Confira também



[Sobre a máquina de estado de replicação](about-the-replication-state-machine.md)
  
[Constantes de MAPI](mapi-constants.md)
  
[DNTBL](dntbl.md)

