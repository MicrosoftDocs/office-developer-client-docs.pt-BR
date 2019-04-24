---
title: Determinar se um item do Outlook foi modificado, mas não salvo (referência do Outlook auxiliar)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 65fba557-5fb0-42de-8715-eccda1f3c648
description: Este tópico mostra como usar a identificação de expedição de dispidFDirty para chamar a propriedade correspondente em um item do Outlook, para ver se o item foi modificado e não foi salvo.
ms.openlocfilehash: e66a23983a3cc19a7cb51d4b4c3b2c1cee58a793
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317637"
---
# <a name="determine-if-an-outlook-item-has-been-modified-but-not-saved-outlook-auxiliary-reference"></a>Determinar se um item do Outlook foi modificado, mas não salvo (referência do Outlook auxiliar)

Este tópico mostra como usar a identificação de expedição de **dispidFDirty** para chamar a propriedade correspondente em um item do Outlook, para ver se o item foi modificado e não foi salvo. 
  
Dado um objeto de item, você pode usar o método [IUnknown::QueryInterface](https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q_)) para obter um ponteiro de interface [IDispatch](https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) . A função no tópico `FIsItemDirty` aceita um ponteiro **IDispatch** , _pdisp_, como um parâmetro de entrada.  `FIsItemDirty` chama o método [IDispatch:: Invoke](https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke) , especificando a **dispidFDirty** como o argumento para o parâmetro  _dispIdMember_ e os sinalizadores  `DISPATCH_METHOD | DISPATCH_PROPERTYGET` para  _wFlags_, para verificar se o item foi modificado.  `FIsItemDirty`Retorna um valor Boolean (**true** para indicar que o item possui alterações não salvas; caso contrário, **false**).
  
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

