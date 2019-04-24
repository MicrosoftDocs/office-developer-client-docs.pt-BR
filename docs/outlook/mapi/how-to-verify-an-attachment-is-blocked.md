---
title: Verificar se um anexo foi bloqueado
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 69663470-45f3-86ed-e015-eba32b5a7233
description: '�ltima altera��o: segunda-feira, 25 de junho de 2012'
ms.openlocfilehash: c1c6f960f2e24108bebdc8f6cbf08bf1d94d85ae
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345882"
---
# <a name="verify-an-attachment-is-blocked"></a>Verificar se um anexo foi bloqueado

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Este exemplo de código no C++ mostra como usar a interface [IAttachmentSecurity: IUnknown](iattachmentsecurityiunknown.md) para descobrir se um anexo é bloqueado pelo microsoft Outlook 2010 ou pelo microsoft Outlook 2013 para exibição e indexação. 
  
[IAttachmentSecurity: IUnknown](iattachmentsecurityiunknown.md) é derivado da interface [IUnknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx) . Você pode obter a interface [IAttachmentSecurity: IUnknown](iattachmentsecurityiunknown.md) chamando [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) no objeto de sessão MAPI, solicitando o **IID_IAttachmentSecurity**. [IAttachmentSecurity:: IsAttachmentBlocked](iattachmentsecurity-isattachmentblocked.md) retorna **true** no _pfBlocked_ se o anexo é considerado não seguro pelo Outlook 2010 ou pelo Outlook 2013 e é bloqueado para exibição e indexação no Outlook 2010 ou no Outlook 2013. 
  
```cpp
HRESULT IsAttachmentBlocked(LPMAPISESSION lpMAPISession, LPCWSTR pwszFileName, BOOL* pfBlocked) 
{ 
    if (!lpMAPISession || !pwszFileName || !pfBlocked) return MAPI_E_INVALID_PARAMETER; 
 
    HRESULT hRes = S_OK; 
    IAttachmentSecurity* lpAttachSec = NULL; 
    BOOL bBlocked = false; 
 
    hRes = lpMAPISession-&gt;QueryInterface(IID_IAttachmentSecurity,(void**)&amp;lpAttachSec); 
    if (SUCCEEDED(hRes) &amp;&amp; lpAttachSec) 
    { 
        hRes = lpAttachSec-&gt;IsAttachmentBlocked(pwszFileName,&amp;bBlocked); 
    } 
    if (lpAttachSec) lpAttachSec-&gt;Release(); 
 
    *pfBlocked = bBlocked; 
    return hRes; 
}

```


