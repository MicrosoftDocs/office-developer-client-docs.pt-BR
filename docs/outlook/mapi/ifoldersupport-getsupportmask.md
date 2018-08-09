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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 6f7aa23606da40c817c9af623b8bade9383ce427
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766928"
---
# <a name="ifoldersupportgetsupportmask"></a>IFolderSupport::GetSupportMask

  
  
**Aplica-se a**: Outlook 
  
Obtém informações sobre o suporte de uma pasta para compartilhamento.
  
```cpp
HRESULT GetSupportMask( 
    DWORD * pdwSupportMask 
); 
```

## <a name="parameters"></a>Parâmetros

 _pdwSupportMask_
  
> [out] Uma máscara de bits que indica se a pasta oferece suporte a compartilhamento.
    
 **FS_NONE**
  
> Indica que a pasta não oferece suporte a compartilhamento.
    
 **FS_SUPPORTS_SHARING**
  
> Indica que a pasta suporta compartilhamento.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A chamada foi bem-sucedida.
    

