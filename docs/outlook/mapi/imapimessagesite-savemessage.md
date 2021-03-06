---
title: IMAPIMessageSiteSaveMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.SaveMessage
api_type:
- COM
ms.assetid: 94c44952-d297-4705-9778-90373dfa5ad6
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 938eaa6c1a39d24157d5d690c42b435af6192cb6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417102"
---
# <a name="imapimessagesitesavemessage"></a>IMAPIMessageSite::SaveMessage

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Solicita que a mensagem atual seja salva.
  
```cpp
HRESULT SaveMessage( void );
```

## <a name="parameters"></a>Parâmetros

Nenhum.
  
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor ou os valores esperados. 
    
## <a name="remarks"></a>Comentários

Os formulários chamam **o método IMAPIMessageSite::SaveMessage** para solicitar que uma mensagem seja salva. 
  
Para uma lista de interfaces relacionadas a servidores de formulário, consulte [MAPI Form Interfaces](mapi-form-interfaces.md).
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::SaveMessage  <br/> |MFCMAPI usa o **método IMAPIMessageSite::SaveMessage** para salvar a mensagem.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)
  
[Interfaces de formulário MAPI](mapi-form-interfaces.md)

