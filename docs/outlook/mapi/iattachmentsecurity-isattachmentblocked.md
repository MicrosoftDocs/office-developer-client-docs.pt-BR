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
ms.openlocfilehash: d255d7b6e80fe0c080fa0a27a7976db758a8c2ec
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439776"
---
# <a name="iattachmentsecurityisattachmentblocked"></a>IAttachmentSecurity::IsAttachmentBlocked

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Verifica se um anexo especificado está bloqueado pelo Microsoft Outlook 2010 ou Microsoft Outlook 2013 para exibição e indexação.
  
```cpp
HRESULT IAttachmentSecurity::IsAttachmentBlocked( 
    LPCWSTR pwszFileName,  
    BOOL *pfBlocked 
);
```

## <a name="parameters"></a>Parâmetros

 _pwszFileName_
  
> no Ponteiro para o nome de arquivo de um anexo.
    
 _pfBlocked_
  
> bota Ponteiro para um valor que indica **true** se o anexo especificado estiver bloqueado; caso contrário, **false**.
    
## <a name="see-also"></a>Confira também



[Constantes de MAPI](mapi-constants.md)
  
[Verificar se um anexo está bloqueado](how-to-verify-an-attachment-is-blocked.md)

