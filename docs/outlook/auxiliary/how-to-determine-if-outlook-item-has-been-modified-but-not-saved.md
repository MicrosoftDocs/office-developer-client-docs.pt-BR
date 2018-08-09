---
title: Determinar se um item do Outlook foi modificado, mas não salvo (referência auxiliar do Outlook)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 65fba557-5fb0-42de-8715-eccda1f3c648
description: Este tópico mostra como usar a identificação de expedição de dispidFDirty para chamar a propriedade correspondente em um item do Outlook, para ver se o item foi modificado e não foi salvo.
ms.openlocfilehash: ece6ede368cf2ffb3b18575161fef4b3f132fdf0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765807"
---
# <a name="determine-if-an-outlook-item-has-been-modified-but-not-saved-outlook-auxiliary-reference"></a><span data-ttu-id="55465-103">Determinar se um item do Outlook foi modificado, mas não salvo (referência auxiliar do Outlook)</span><span class="sxs-lookup"><span data-stu-id="55465-103">Determine if an Outlook item has been modified but not saved (Outlook Auxiliary Reference)</span></span>

<span data-ttu-id="55465-104">Este tópico mostra como usar a identificação de expedição de **dispidFDirty** para chamar a propriedade correspondente em um item do Outlook, para ver se o item foi modificado e não foi salvo.</span><span class="sxs-lookup"><span data-stu-id="55465-104">This topic shows how to use the **dispidFDirty** dispatch ID to invoke the corresponding property on an Outlook item, to see whether the item has been modified and has not been saved.</span></span> 
  
<span data-ttu-id="55465-105">Dado um objeto de item, você pode usar o método [IUnknown::QueryInterface](http://msdn.microsoft.com/library/com.iunknown_queryinterface.aspx) para obter um ponteiro de interface [IDispatch](http://msdn.microsoft.com/library/ebbff4bc-36b2-4861-9efa-ffa45e013eb5%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="55465-105">Given an item object, you can use the [IUnknown::QueryInterface](http://msdn.microsoft.com/library/com.iunknown_queryinterface.aspx) method to obtain an [IDispatch](http://msdn.microsoft.com/library/ebbff4bc-36b2-4861-9efa-ffa45e013eb5%28Office.15%29.aspx) interface pointer.</span></span> <span data-ttu-id="55465-106">A função no tópico `FIsItemDirty` aceita um ponteiro **IDispatch** , _pdisp_, como um parâmetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="55465-106">The function in the topic `FIsItemDirty` accepts an **IDispatch** pointer,  _pdisp_, as an input parameter.</span></span>  <span data-ttu-id="55465-107">`FIsItemDirty` chama o método [IDispatch:: Invoke](http://msdn.microsoft.com/library/964ade8e-9d8a-4d32-bd47-aa678912a54d%28Office.15%29.aspx) , especificando a **dispidFDirty** como o argumento para o parâmetro  _dispIdMember_ e os sinalizadores  `DISPATCH_METHOD | DISPATCH_PROPERTYGET` para  _wFlags_, para verificar se o item foi modificado.</span><span class="sxs-lookup"><span data-stu-id="55465-107">`FIsItemDirty` calls the [IDispatch::Invoke](http://msdn.microsoft.com/library/964ade8e-9d8a-4d32-bd47-aa678912a54d%28Office.15%29.aspx) method, specifying **dispidFDirty** as the argument for the  _dispIdMember_ parameter, and the flags  `DISPATCH_METHOD | DISPATCH_PROPERTYGET` for  _wFlags_, to verify whether the item has been modified.</span></span>  <span data-ttu-id="55465-108">`FIsItemDirty`Retorna um valor booleano (**True** para indicar que o item possui alterações não salvas; caso contrário, **False**).</span><span class="sxs-lookup"><span data-stu-id="55465-108">`FIsItemDirty` returns a Boolean value (**True** to indicate that the item has unsaved changes; otherwise, **False**).</span></span>
  
```cpp
bool FIsItemDirty(IDispatch *pdisp)
{
    DISPPARAMS dispparams;
    UINT uArgErr;
    HRESULT hr = S_OK;
    CComVariant varDirty;
    dispparams.rgvarg = 0;
    dispparams.cArgs = 0;
    dispparams.cNamedArgs = 0;
    dispparams.rgdispidNamedArgs = NULL;
    hr = pdisp->Invoke(dispidFDirty,
        IID_NULL,
        LOCALE_SYSTEM_DEFAULT,
        DISPATCH_METHOD | DISPATCH_PROPERTYGET,
        &amp;dispparams,
        &amp;varDirty,
        NULL,
        &amp;uArgErr);
    return SUCCEEDED(hr) &amp;&amp; varDirty.bVal;
}

```

## <a name="see-also"></a><span data-ttu-id="55465-109">Confira também</span><span class="sxs-lookup"><span data-stu-id="55465-109">See also</span></span>

- [<span data-ttu-id="55465-110">Constantes (Outlook exportados APIs)</span><span class="sxs-lookup"><span data-stu-id="55465-110">Constants (Outlook exported APIs)</span></span>](constants-outlook-exported-apis.md)

