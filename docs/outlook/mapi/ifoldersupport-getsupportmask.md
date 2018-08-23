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
ms.openlocfilehash: c51f4a7266e67be08f31daa5afbf23ce0b256252
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567850"
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
  
> [out] Uma máscara de bits que indica se a pasta oferece suporte a compartilhamento.
    
 **FS_NONE**
  
> Indica que a pasta não oferece suporte a compartilhamento.
    
 **FS_SUPPORTS_SHARING**
  
> Indica que a pasta suporta compartilhamento.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A chamada foi bem-sucedida.
    

