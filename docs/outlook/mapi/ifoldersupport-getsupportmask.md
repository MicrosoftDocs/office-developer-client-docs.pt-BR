---
title: IFolderSupportGetSupportMask
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IFolderSupport.GetSupportMask
api_type:
- COM
ms.assetid: 8d8aaeb7-57d7-ba4c-95d1-a5368cfc4afe
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 1c27bdc52ebe725c40cbf318fab0678f41cdc287
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417368"
---
# <a name="ifoldersupportgetsupportmask"></a>IFolderSupport::GetSupportMask

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Obtém informações sobre o suporte de uma pasta para compartilhamento.
  
```cpp
HRESULT GetSupportMask( 
    DWORD * pdwSupportMask 
); 
```

## <a name="parameters"></a>Parâmetros

 _pdwSupportMask_
  
> [out] Uma máscara de bits indicando se a pasta oferece suporte ao compartilhamento.
    
 **FS_NONE**
  
> Indica que a pasta não tem suporte para compartilhamento.
    
 **FS_SUPPORTS_SHARING**
  
> Indica que a pasta oferece suporte ao compartilhamento.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada foi bem-sucedida.
    

