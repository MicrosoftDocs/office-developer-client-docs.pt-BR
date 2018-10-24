---
title: Verificar se um anexo foi bloqueado
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 69663470-45f3-86ed-e015-eba32b5a7233
description: 'Última modificação: 25 de julho de 2012'
ms.openlocfilehash: c1c6f960f2e24108bebdc8f6cbf08bf1d94d85ae
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393835"
---
# <a name="verify-an-attachment-is-blocked"></a>Verificar se um anexo foi bloqueado

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
No C++, este exemplo de código mostra como usar o [IAttachmentSecurity: IUnknown](iattachmentsecurityiunknown.md) interface para descobrir se um anexo estiver bloqueado pelo Microsoft Outlook 2010 ou o Microsoft Outlook 2013 para exibição e indexação. 
  
[IAttachmentSecurity: IUnknown](iattachmentsecurityiunknown.md) é derivado da interface [IUnknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx) . Você pode obter o [IAttachmentSecurity: IUnknown](iattachmentsecurityiunknown.md) interface chamando [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) no objeto sessão MAPI, solicitando **IID_IAttachmentSecurity**. [IAttachmentSecurity::IsAttachmentBlocked](iattachmentsecurity-isattachmentblocked.md) retorna **true** em _pfBlocked_ se o anexo é considerado inseguro pelo Outlook 2010 ou Outlook 2013 e seja bloqueado para exibição e indexação no Outlook 2010 ou Outlook 2013. 
  
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


