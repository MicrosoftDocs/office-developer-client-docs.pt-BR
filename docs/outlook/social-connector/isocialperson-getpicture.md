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
ms.openlocfilehash: 755e2138378136a3c1d810a1957923f4e8db721d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331651"
---
# <a name="isocialpersongetpicture"></a>ISocialPerson::GetPicture

Obtém uma matriz de bytes que contém o recurso de imagem para a pessoa. 
  
```cpp
HRESULT _stdcall GetPicture([out, retval] SAFEARRAY(unsigned char)* picture);
```

## <a name="parameters"></a>Parâmetros

_Panorama_
  
> bota Um ponteiro para uma estrutura que especifica uma matriz de bytes que representa o recurso de imagem para uma pessoa.
    
## <a name="remarks"></a>Comentários

Os recursos de imagem suportados estão no formato. bmp,. jpeg ou. png.
  
## <a name="see-also"></a>Confira também

- [ISocialPerson : IUnknown](isocialpersoniunknown.md)

