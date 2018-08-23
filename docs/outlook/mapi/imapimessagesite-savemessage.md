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
ms.openlocfilehash: 9fa7c7226c4ddb5acf5c6b73f55c46829d959eef
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572302"
---
# <a name="imapimessagesitesavemessage"></a>IMAPIMessageSite::SaveMessage

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Solicita que a mensagem atual seja salvo.
  
```cpp
HRESULT SaveMessage( void );
```

## <a name="parameters"></a>Parâmetros

Nenhum.
  
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores. 
    
## <a name="remarks"></a>Comentários

Formulários chame o método de **IMAPIMessageSite::SaveMessage** para solicitar que uma mensagem seja salvo. 
  
Para obter uma lista das interfaces relacionadas aos servidores de formulário, consulte [Interfaces de formulário de MAPI](mapi-form-interfaces.md).
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::SaveMessage  <br/> |MFCMAPI usa o método **IMAPIMessageSite::SaveMessage** para salvar a mensagem.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)
  
[Interfaces de formulário MAPI](mapi-form-interfaces.md)

