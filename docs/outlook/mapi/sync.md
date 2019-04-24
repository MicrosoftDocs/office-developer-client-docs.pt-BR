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
ms.openlocfilehash: e856044a1b6345c4e495a75dfb7ca0defa52ceec
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349592"
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
  
- [out]/[in] um bitmask dos seguintes sinalizadores que modifica o comportamento durante a sincronização:
    
- UPS_UPLOAD_ONLY
    
  - no O cliente executará o carregamento apenas. O Outlook retorna apenas as pastas modificadas localmente.
    
- UPS_DNLOAD_ONLY
    
  - no O cliente executará apenas o download. O Outlook não deve limpar bits de carregamento para pastas.
    
- UPS_THESE_FOLDERS
    
  - no O cliente estará sincronizando um conjunto de pastas especificado com as IDs de entrada fornecidas. Esse sinalizador pode ser combinado com o sinalizador **UPS_UPLOAD_ONLY** ou **UPS_DNLOAD_ONLY** . 
    
- UPS_OK
    
  - bota A sincronização foi bem-sucedida. O cliente define isso após o carregamento ou uma sincronização completa ser concluída.
    
- 
    
    > [!NOTE]
    > Embora o cliente possa carregar ou sincronizar totalmente (carregar e baixar) pastas e itens com a API de replicação, o cliente especifica *parâmetroulflags* com apenas uma direção da replicação de cada vez, ou seja, o **UPS_UPLOAD_ONLY** ou Sinalizador **UPS_DNLOAD_ONLY** . No caso de uma sincronização completa, o cliente primeiro realiza um upload com o sinalizador **UPS_UPLOAD_ONLY** e, em seguida, um download com o sinalizador **UPS_DNLOAD_ONLY** . 
  
 _pwzPath_
  
- bota Caminho para o repositório local.
    
 _Reserved1_
  
- Este membro é reservado para uso interno do Outlook e não tem suporte.
    
 _Reserved2_
  
- Este membro é reservado para uso interno do Outlook e não tem suporte.
    
 *PEL* 
  
- no Esta é a lista de IDs de entrada das pastas a serem sincronizadas se **UPS_THESE_FOLDERS** tiver sido definido. Consulte mapidefs. h para a definição de tipo de **LPENTRYLIST**. 
    
 _pulFolderOptions_
  
- no Esta é uma matriz de opções de pasta para pastas correspondentes no *PEL* se **UPS_THESE_FOLDERS** tiver sido definido. Essas opções de pasta são usadas ao carregar cada uma das pastas listadas em *PEL* durante o [estado de carregamento da pasta](upload-folder-state.md). Para obter mais informações sobre opções de pasta, consulte **[UPFLD](upfld.md)**. 
    
## <a name="see-also"></a>Confira também



[Sobre a API de replicação](about-the-replication-api.md)
  
[Sobre a máquina de estado de replicação](about-the-replication-state-machine.md)
  
[Constantes de MAPI](mapi-constants.md)

