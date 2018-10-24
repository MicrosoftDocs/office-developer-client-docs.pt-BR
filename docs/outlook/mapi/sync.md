---
title: SYNC
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3f07fddf-4c42-6ea7-162d-57022166a83f
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: a40046a26efe118e48cdca4749d2e99212bb8bfe
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579835"
---
# <a name="sync"></a>SYNC

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Informações para iniciar a sincronização entre um repositório local e um servidor. Essas informações são usadas durante o [estado de sincronização](synchronize-state.md).
  
## <a name="quick-info"></a>Informações rápidas

```cpp
struct SYNC 
{ 
    ULONG ulFlags; 
    LPWSTR pwzPath; 
    FEID Reserved1; 
    MEID Reserved2; 
    LPENTRYLIST pel; 
    ULONG const * pulFolderOptions; 
};
```

## <a name="members"></a>Membros

 _ulFlags_
  
- [out] / [in] uma bitmask dos seguintes sinalizadores que modifica o comportamento durante a sincronização:
    
- UPS_UPLOAD_ONLY
    
  - [in] O cliente realizarão somente carregamento. Outlook retorna apenas pastas modificadas localmente.
    
- UPS_DNLOAD_ONLY
    
  - [in] O cliente realizarão somente download. Outlook não deve limpar os bits de carregamento de pastas.
    
- UPS_THESE_FOLDERS
    
  - [in] O cliente será sincronizando um conjunto especificado de pastas com as IDs da entrada fornecida. Este sinalizador pode ser combinado com o **UPS_UPLOAD_ONLY** ou **UPS_DNLOAD_ONLY** sinalizador. 
    
- UPS_OK
    
  - [out] Sincronização foi bem-sucedida. O cliente define esta após carregar ou conclui uma sincronização completa.
    
- 
    
    > [!NOTE]
    > Mesmo que o cliente pode carregar ou totalmente sincronizar (carregar e baixar) pastas e itens com a API de replicação, o cliente especifica *ulFlags* com apenas uma direção da replicação ao mesmo tempo — o **UPS_UPLOAD_ONLY** ou Sinalizador **UPS_DNLOAD_ONLY** . No caso de uma sincronização completa, o cliente primeiro faz um carregamento com o sinalizador **UPS_UPLOAD_ONLY** e, em seguida, um download com o sinalizador **UPS_DNLOAD_ONLY** . 
  
 _pwzPath_
  
- [out] Caminho para o armazenamento local.
    
 _Reserved1_
  
- Este membro é reservado para uso interno do Outlook e não é suportado.
    
 _Reserved2_
  
- Este membro é reservado para uso interno do Outlook e não é suportado.
    
 *PEL* 
  
- [in] Esta é a lista de IDs das pastas para sincronizar se **UPS_THESE_FOLDERS** tiver sido definida de entrada. Consulte mapidefs.h para a definição de tipo de **LPENTRYLIST**. 
    
 _pulFolderOptions_
  
- [in] Isso é uma matriz das opções de pasta para pastas correspondentes no *pel* se **UPS_THESE_FOLDERS** tiver sido definida. Essas opções de pasta são usadas quando o carregamento de cada uma das pastas listadas no *pel* durante o [carregamento do estado da pasta](upload-folder-state.md). Para obter mais informações sobre opções de pasta, consulte **[UPFLD](upfld.md)**. 
    
## <a name="see-also"></a>Confira também



[Sobre a API de replicação](about-the-replication-api.md)
  
[Sobre a máquina de estado de replicação](about-the-replication-state-machine.md)
  
[Constantes de MAPI](mapi-constants.md)

