---
title: ISocialPersonGetPicture
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 02fcaf25-42b5-4584-95c6-d44a3d035128
description: Obtém uma matriz de bytes que contém o recurso de imagem da pessoa.
ms.openlocfilehash: 755e2138378136a3c1d810a1957923f4e8db721d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406707"
---
# <a name="isocialpersongetpicture"></a>ISocialPerson::GetPicture

Obtém uma matriz de bytes que contém o recurso de imagem da pessoa. 
  
```cpp
HRESULT _stdcall GetPicture([out, retval] SAFEARRAY(unsigned char)* picture);
```

## <a name="parameters"></a>Parâmetros

_imagem_
  
> [out] Um ponteiro para uma estrutura que especifica uma matriz de bytes que representa o recurso de imagem de uma pessoa.
    
## <a name="remarks"></a>Comentários

Os recursos de imagem com suporte estão nos formatos .bmp, .jpeg ou .png.
  
## <a name="see-also"></a>Confira também

- [ISocialPerson : IUnknown](isocialpersoniunknown.md)

