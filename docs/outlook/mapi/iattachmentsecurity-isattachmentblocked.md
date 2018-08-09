---
title: IAttachmentSecurityIsAttachmentBlocked
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAttachmentSecurity.IsAttachmentBlocked
api_type:
- COM
ms.assetid: 6986d27a-9602-e44a-0797-4c47f2184ef7
description: '�ltima altera��o: segunda-feira, 25 de junho de 2012'
ms.openlocfilehash: 45e4362fc025c1784e9432c5d641e865a044bd00
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766903"
---
# <a name="iattachmentsecurityisattachmentblocked"></a>IAttachmentSecurity::IsAttachmentBlocked

  
  
**Aplica-se a**: Outlook 
  
Verifica se um anexo especificado será bloqueado pelo Microsoft Outlook 2010 ou o Microsoft Outlook 2013 para exibição e indexação.
  
```cpp
HRESULT IAttachmentSecurity::IsAttachmentBlocked( 
    LPCWSTR pwszFileName,  
    BOOL *pfBlocked 
);
```

## <a name="parameters"></a>Parâmetros

 _pwszFileName_
  
> [in] Ponteiro para o nome de arquivo de anexo.
    
 _pfBlocked_
  
> [out] Ponteiro para um valor que indica **true** se o anexo especificado está bloqueado; Caso contrário, **false**.
    
## <a name="see-also"></a>Confira também



[Constantes MAPI](mapi-constants.md)
  
[Verificar se um anexo foi bloqueado](how-to-verify-an-attachment-is-blocked.md)

