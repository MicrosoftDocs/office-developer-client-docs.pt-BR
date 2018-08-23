---
title: Verifique se que um anexo estiver bloqueado
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 69663470-45f3-86ed-e015-eba32b5a7233
description: '�ltima altera��o: segunda-feira, 25 de junho de 2012'
ms.openlocfilehash: bb83b57de3bb484e4fb5f94f76a7d9bfa0fce876
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589795"
---
# <a name="verify-an-attachment-is-blocked"></a><span data-ttu-id="a884c-103">Verifique se que um anexo estiver bloqueado</span><span class="sxs-lookup"><span data-stu-id="a884c-103">Verify an attachment is blocked</span></span>

<span data-ttu-id="a884c-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a884c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a884c-105">No C++, este exemplo de código mostra como usar o [IAttachmentSecurity: IUnknown](iattachmentsecurityiunknown.md) interface para descobrir se um anexo estiver bloqueado pelo Microsoft Outlook 2010 ou o Microsoft Outlook 2013 para exibição e indexação.</span><span class="sxs-lookup"><span data-stu-id="a884c-105">This code sample in C++ shows how to use the [IAttachmentSecurity : IUnknown](iattachmentsecurityiunknown.md) interface to find out whether an attachment is blocked by Microsoft Outlook 2010 or Microsoft Outlook 2013 for viewing and indexing.</span></span> 
  
<span data-ttu-id="a884c-106">[IAttachmentSecurity: IUnknown](iattachmentsecurityiunknown.md) é derivado da interface [IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="a884c-106">[IAttachmentSecurity : IUnknown](iattachmentsecurityiunknown.md) is derived from the [IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28VS.85%29.aspx) interface.</span></span> <span data-ttu-id="a884c-107">Você pode obter o [IAttachmentSecurity: IUnknown](iattachmentsecurityiunknown.md) interface chamando [IUnknown:: QueryInterface](http://msdn.microsoft.com/en-us/library/ms682521%28v=VS.85%29.aspx) no objeto sessão MAPI, solicitando **IID_IAttachmentSecurity**.</span><span class="sxs-lookup"><span data-stu-id="a884c-107">You can obtain the [IAttachmentSecurity : IUnknown](iattachmentsecurityiunknown.md) interface by calling [IUnknown::QueryInterface](http://msdn.microsoft.com/en-us/library/ms682521%28v=VS.85%29.aspx) on the MAPI session object, requesting **IID_IAttachmentSecurity**.</span></span> <span data-ttu-id="a884c-108">[IAttachmentSecurity::IsAttachmentBlocked](iattachmentsecurity-isattachmentblocked.md) retorna **true** em _pfBlocked_ se o anexo é considerado inseguro pelo Outlook 2010 ou Outlook 2013 e seja bloqueado para exibição e indexação no Outlook 2010 ou Outlook 2013.</span><span class="sxs-lookup"><span data-stu-id="a884c-108">[IAttachmentSecurity::IsAttachmentBlocked](iattachmentsecurity-isattachmentblocked.md) returns **true** in  _pfBlocked_ if the attachment is considered unsafe by Outlook 2010 or Outlook 2013 and is blocked for viewing and indexing in Outlook 2010 or Outlook 2013.</span></span> 
  
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


