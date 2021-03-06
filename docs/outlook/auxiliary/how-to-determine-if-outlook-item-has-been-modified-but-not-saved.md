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
# <a name="determine-if-an-outlook-item-has-been-modified-but-not-saved-outlook-auxiliary-reference"></a>Determinar se um item do Outlook foi modificado, mas não salvo (Referência Auxiliar do Outlook)

Este tópico mostra como usar a identificação de expedição de **dispidFDirty** para chamar a propriedade correspondente em um item do Outlook, para ver se o item foi modificado e não foi salvo. 
  
Dado um objeto de item, você pode usar o método [IUnknown::QueryInterface](https://docs.microsoft.com/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para obter um ponteiro de interface [IDispatch](https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) . A função no tópico `FIsItemDirty` aceita um ponteiro **IDispatch,**  _pdisp,_ como um parâmetro de entrada.  `FIsItemDirty` chama o método [IDispatch:: Invoke](https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke) , especificando a **dispidFDirty** como o argumento para o parâmetro  _dispIdMember_ e os sinalizadores  `DISPATCH_METHOD | DISPATCH_PROPERTYGET` para  _wFlags_, para verificar se o item foi modificado.  `FIsItemDirty` retorna um valor Boolean (**True** para indicar que o item tem alterações não-salvas; caso contrário, **False**).
  
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

## <a name="see-also"></a>Confira também

- [Constantes (Outlook exportados APIs)](constants-outlook-exported-apis.md)

