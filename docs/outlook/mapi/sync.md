---
title: SYNC
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3f07fddf-4c42-6ea7-162d-57022166a83f
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: c856dfd1d419fd7a4bf4f47852ffb69470f9281b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770559"
---
# <a name="sync"></a>SYNC

  
  
**Aplica-se a**: Outlook 
  
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

## <a name="members"></a>Members

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
  
[Constantes MAPI](mapi-constants.md)

