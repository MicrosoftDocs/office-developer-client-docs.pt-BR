---
title: ISocialProviderDefaultSiteUrls
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 322ea2e9-d6c9-48f9-a927-7162346d16a4
description: Retorna uma matriz de cadeias de caracteres que especificam URLs de site para o provedor do Outlook Social Connector (OSC).
ms.openlocfilehash: 34d779d5eb42b81a14c5236685104e9ef4fe36f2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413770"
---
# <a name="isocialproviderdefaultsiteurls"></a>ISocialProvider::DefaultSiteUrls

Retorna uma matriz de cadeias de caracteres que especificam URLs de site para o provedor do Outlook Social Connector (OSC).
  
```cpp
[propget] HRESULT _stdcall DefaultSiteUrls([out, retval] SAFEARRAY(BSTR)* siteUrls);
```

## <a name="property-value"></a>Valor de propriedade

Um ponteiro para uma estrutura que especifica uma matriz de cadeias de caracteres que representam URLs de site para o provedor OSC.
  
## <a name="remarks"></a>Comentários

Um provedor pode dar suporte A URLs de vários sites. O OSC define a propriedade [ISocialSession:: SiteUrl](isocialsession-siteurl.md) para informar o provedor da URL do site selecionada. 
  
O OSC usa o primeiro elemento da matriz como a URL do site padrão. Um provedor pode retornar elementos adicionais na matriz de URL do site, mas o OSC não os usa. 
  
## <a name="see-also"></a>Confira também

- [ISocialProvider : IUnknown](isocialprovideriunknown.md)

