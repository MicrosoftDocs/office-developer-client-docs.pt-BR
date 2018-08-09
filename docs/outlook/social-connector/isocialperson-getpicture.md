---
title: ISocialPersonGetPicture
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 02fcaf25-42b5-4584-95c6-d44a3d035128
description: Obtém uma matriz de bytes que contém o recurso de imagem para a pessoa.
ms.openlocfilehash: dcb0da5bc36c2166d569c770d1f182cd21339435
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770833"
---
# <a name="isocialpersongetpicture"></a>ISocialPerson::GetPicture

Obtém uma matriz de bytes que contém o recurso de imagem para a pessoa. 
  
```cpp
HRESULT _stdcall GetPicture([out, retval] SAFEARRAY(unsigned char)* picture);
```

## <a name="parameters"></a>Parâmetros

_imagem_
  
> [out] Um ponteiro para uma estrutura que especifica uma matriz de bytes que representam o recurso de imagem de uma pessoa.
    
## <a name="remarks"></a>Comentários

Suporte para imagem recursos estão no formato. png,. JPEG ou. bmp.
  
## <a name="see-also"></a>Confira também

- [ISocialPerson : IUnknown](isocialpersoniunknown.md)

