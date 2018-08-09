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
# <a name="isocialpersongetpicture"></a><span data-ttu-id="30bdf-103">ISocialPerson::GetPicture</span><span class="sxs-lookup"><span data-stu-id="30bdf-103">ISocialPerson::GetPicture</span></span>

<span data-ttu-id="30bdf-104">Obtém uma matriz de bytes que contém o recurso de imagem para a pessoa.</span><span class="sxs-lookup"><span data-stu-id="30bdf-104">Gets an array of bytes that contains the picture resource for the person.</span></span> 
  
```cpp
HRESULT _stdcall GetPicture([out, retval] SAFEARRAY(unsigned char)* picture);
```

## <a name="parameters"></a><span data-ttu-id="30bdf-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="30bdf-105">Parameters</span></span>

<span data-ttu-id="30bdf-106">_imagem_</span><span class="sxs-lookup"><span data-stu-id="30bdf-106">_picture_</span></span>
  
> <span data-ttu-id="30bdf-107">[out] Um ponteiro para uma estrutura que especifica uma matriz de bytes que representam o recurso de imagem de uma pessoa.</span><span class="sxs-lookup"><span data-stu-id="30bdf-107">[out] A pointer to a structure that specifies an array of bytes that represent the picture resource for a person.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="30bdf-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="30bdf-108">Remarks</span></span>

<span data-ttu-id="30bdf-109">Suporte para imagem recursos estão no formato. png,. JPEG ou. bmp.</span><span class="sxs-lookup"><span data-stu-id="30bdf-109">Supported picture resources are in .bmp, .jpeg, or .png format.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="30bdf-110">Confira também</span><span class="sxs-lookup"><span data-stu-id="30bdf-110">See also</span></span>

- [<span data-ttu-id="30bdf-111">ISocialPerson : IUnknown</span><span class="sxs-lookup"><span data-stu-id="30bdf-111">ISocialPerson : IUnknown</span></span>](isocialpersoniunknown.md)

