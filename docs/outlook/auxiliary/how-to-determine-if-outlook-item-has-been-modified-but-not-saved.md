---
title: Determinar se um item do Outlook foi modificado, mas não salvo (Referência Auxiliar do Outlook)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 65fba557-5fb0-42de-8715-eccda1f3c648
description: Este tópico mostra como usar a identificação de expedição de dispidFDirty para chamar a propriedade correspondente em um item do Outlook, para ver se o item foi modificado e não foi salvo.
ms.openlocfilehash: 5dc20a45342e0434ab19d7c2347e98dec27b61b8
ms.sourcegitcommit: 007aa2ceb4f569201c3f4372de5c83b6c61f8875
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/02/2020
ms.locfileid: "43102944"
---
# <a name="determine-if-an-outlook-item-has-been-modified-but-not-saved-outlook-auxiliary-reference"></a><span data-ttu-id="85cd2-103">Determinar se um item do Outlook foi modificado, mas não salvo (Referência Auxiliar do Outlook)</span><span class="sxs-lookup"><span data-stu-id="85cd2-103">Determine if an Outlook item has been modified but not saved (Outlook Auxiliary Reference)</span></span>

<span data-ttu-id="85cd2-104">Este tópico mostra como usar a identificação de expedição de **dispidFDirty** para chamar a propriedade correspondente em um item do Outlook, para ver se o item foi modificado e não foi salvo.</span><span class="sxs-lookup"><span data-stu-id="85cd2-104">This topic shows how to use the **dispidFDirty** dispatch ID to invoke the corresponding property on an Outlook item, to see whether the item has been modified and has not been saved.</span></span> 
  
<span data-ttu-id="85cd2-105">Dado um objeto de item, você pode usar o método [IUnknown::QueryInterface](https://docs.microsoft.com/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para obter um ponteiro de interface [IDispatch](https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="85cd2-105">Given an item object, you can use the [IUnknown::QueryInterface](https://docs.microsoft.com/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method to obtain an [IDispatch](https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) interface pointer.</span></span> <span data-ttu-id="85cd2-106">A função no tópico `FIsItemDirty` aceita um ponteiro **IDispatch,**  _pdisp,_ como um parâmetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="85cd2-106">The function in the topic `FIsItemDirty` accepts an **IDispatch** pointer,  _pdisp_, as an input parameter.</span></span>  <span data-ttu-id="85cd2-107">`FIsItemDirty` chama o método [IDispatch:: Invoke](https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke) , especificando a **dispidFDirty** como o argumento para o parâmetro  _dispIdMember_ e os sinalizadores  `DISPATCH_METHOD | DISPATCH_PROPERTYGET` para  _wFlags_, para verificar se o item foi modificado.</span><span class="sxs-lookup"><span data-stu-id="85cd2-107">`FIsItemDirty` calls the [IDispatch::Invoke](https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke) method, specifying **dispidFDirty** as the argument for the  _dispIdMember_ parameter, and the flags  `DISPATCH_METHOD | DISPATCH_PROPERTYGET` for  _wFlags_, to verify whether the item has been modified.</span></span>  <span data-ttu-id="85cd2-108">`FIsItemDirty` retorna um valor Boolean (**True** para indicar que o item tem alterações não-salvas; caso contrário, **False**).</span><span class="sxs-lookup"><span data-stu-id="85cd2-108">`FIsItemDirty` returns a Boolean value (**True** to indicate that the item has unsaved changes; otherwise, **False**).</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="85cd2-109">Confira também</span><span class="sxs-lookup"><span data-stu-id="85cd2-109">See also</span></span>

- [<span data-ttu-id="85cd2-110">Constantes (Outlook exportados APIs)</span><span class="sxs-lookup"><span data-stu-id="85cd2-110">Constants (Outlook exported APIs)</span></span>](constants-outlook-exported-apis.md)

