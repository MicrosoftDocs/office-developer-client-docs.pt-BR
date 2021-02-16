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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433805"
---
# <a name="sync"></a>SYNC

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Informações para iniciar a sincronização entre um armazenamento local e um servidor. Essas informações são usadas durante o [estado de sincronização.](synchronize-state.md)
  
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
  
- [out]/[in] Uma máscara de bits dos seguintes sinalizadores que modifica o comportamento durante a sincronização:
    
- UPS_UPLOAD_ONLY
    
  - [in] O cliente executará apenas o upload. O Outlook só retorna pastas modificadas localmente.
    
- UPS_DNLOAD_ONLY
    
  - [in] O cliente executará apenas o download. Outlook should not clear upload bits for folders.
    
- UPS_THESE_FOLDERS
    
  - [in] O cliente sincroniza um conjunto especificado de pastas com as IDs de entrada fornecidas. Esse sinalizador pode ser combinado com o sinalizador **UPS_UPLOAD_ONLY** ou **UPS_DNLOAD_ONLY** sinalização. 
    
- UPS_OK
    
  - [out] A sincronização foi bem-sucedida. O cliente define isso após o carregamento ou uma sincronização completa é concluída.
    
- 
    
    > [!NOTE]
    > Mesmo que o cliente possa carregar ou sincronizar totalmente (carregar e baixar) pastas e itens com a API de Replicação, o cliente especifica *ulFlags* com apenas uma direção da replicação por vez — o sinalizador **UPS_UPLOAD_ONLY** ou **UPS_DNLOAD_ONLY.** No caso de uma sincronização completa, o cliente primeiro faz um upload com o sinalizador **UPS_UPLOAD_ONLY** e, em seguida, um download com o sinalizador **UPS_DNLOAD_ONLY** cliente. 
  
 _pwzPath_
  
- [out] Caminho para o armazenamento local.
    
 _Reserved1_
  
- Este membro é reservado para uso interno do Outlook e não tem suporte.
    
 _Reserved2_
  
- Este membro é reservado para uso interno do Outlook e não tem suporte.
    
 *pel* 
  
- [in] Esta é a lista de IDs de entrada das pastas a sincronizar **se** UPS_THESE_FOLDERS tiver sido definida. Consulte mapidefs.h para a definição de tipo de **LPENTRYLIST**. 
    
 _porqueFolderOptions_
  
- [in] Esta é uma matriz de opções de pasta para pastas correspondentes no  *pel* **UPS_THESE_FOLDERS** tiver sido definida. Essas opções de pasta são usadas ao carregar cada uma das pastas listadas *na pel* durante o [estado da pasta de carregamento.](upload-folder-state.md) Para obter mais informações sobre opções de pasta, consulte **[UPFLD](upfld.md)**. 
    
## <a name="see-also"></a>Confira também



[Sobre a API de replicação](about-the-replication-api.md)
  
[Sobre a máquina de estado de replicação](about-the-replication-state-machine.md)
  
[Constantes de MAPI](mapi-constants.md)

