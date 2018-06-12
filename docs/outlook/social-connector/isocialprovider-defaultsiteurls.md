---
title: ISocialProviderDefaultSiteUrls
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 322ea2e9-d6c9-48f9-a927-7162346d16a4
description: Retorna uma matriz de cadeias de caracteres que especifica as URLs do site para o provedor do Outlook Social Connector (OSC).
ms.openlocfilehash: a2b2e0397c7c67476ac8067a53e2acbd4eddf270
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770834"
---
# <a name="isocialproviderdefaultsiteurls"></a>ISocialProvider::DefaultSiteUrls

Retorna uma matriz de cadeias de caracteres que especifica as URLs do site para o provedor do Outlook Social Connector (OSC).
  
```cpp
[propget] HRESULT _stdcall DefaultSiteUrls([out, retval] SAFEARRAY(BSTR)* siteUrls);
```

## <a name="property-value"></a>Property value

Um ponteiro para uma estrutura que especifica uma matriz de cadeias de caracteres que representam as URLs do site para o provedor do OSC.
  
## <a name="remarks"></a>Coment�rios

Um provedor pode oferecer suporte a várias URLs de site. O OSC define a propriedade [ISocialSession::SiteUrl](isocialsession-siteurl.md) para informar o provedor da URL do site selecionado. 
  
O OSC usa o primeiro elemento da matriz como a URL do site padrão. Um provedor pode retornar elementos adicionais da matriz de URL do site, mas o OSC não usá-los. 
  
## <a name="see-also"></a>Confira também

- [ISocialProvider: IUnknown](isocialprovideriunknown.md)

