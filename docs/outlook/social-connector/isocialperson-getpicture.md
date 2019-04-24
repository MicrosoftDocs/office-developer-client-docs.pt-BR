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
# <a name="isocialpersongetpicture"></a><span data-ttu-id="af6b8-103">ISocialPerson::GetPicture</span><span class="sxs-lookup"><span data-stu-id="af6b8-103">ISocialPerson::GetPicture</span></span>

<span data-ttu-id="af6b8-104">Obtém uma matriz de bytes que contém o recurso de imagem para a pessoa.</span><span class="sxs-lookup"><span data-stu-id="af6b8-104">Gets an array of bytes that contains the picture resource for the person.</span></span> 
  
```cpp
HRESULT _stdcall GetPicture([out, retval] SAFEARRAY(unsigned char)* picture);
```

## <a name="parameters"></a><span data-ttu-id="af6b8-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="af6b8-105">Parameters</span></span>

<span data-ttu-id="af6b8-106">_Panorama_</span><span class="sxs-lookup"><span data-stu-id="af6b8-106">_picture_</span></span>
  
> <span data-ttu-id="af6b8-107">bota Um ponteiro para uma estrutura que especifica uma matriz de bytes que representa o recurso de imagem para uma pessoa.</span><span class="sxs-lookup"><span data-stu-id="af6b8-107">[out] A pointer to a structure that specifies an array of bytes that represent the picture resource for a person.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="af6b8-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="af6b8-108">Remarks</span></span>

<span data-ttu-id="af6b8-109">Os recursos de imagem suportados estão no formato. bmp,. jpeg ou. png.</span><span class="sxs-lookup"><span data-stu-id="af6b8-109">Supported picture resources are in .bmp, .jpeg, or .png format.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="af6b8-110">Confira também</span><span class="sxs-lookup"><span data-stu-id="af6b8-110">See also</span></span>

- [<span data-ttu-id="af6b8-111">ISocialPerson : IUnknown</span><span class="sxs-lookup"><span data-stu-id="af6b8-111">ISocialPerson : IUnknown</span></span>](isocialpersoniunknown.md)

