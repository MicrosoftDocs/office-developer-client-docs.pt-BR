---
title: ISocialSessionGetPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2d0a2945-54d7-417f-b5c6-2647c70263cf
description: Obtém uma interface ISocialPerson com base em que o parâmetro userID.
ms.openlocfilehash: 5769f4c41bb97f45ab722f1b3a3febe24c8a7ab2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770854"
---
# <a name="isocialsessiongetperson"></a><span data-ttu-id="225f4-103">ISocialSession::GetPerson</span><span class="sxs-lookup"><span data-stu-id="225f4-103">ISocialSession::GetPerson</span></span>

<span data-ttu-id="225f4-104">Obtém uma interface [ISocialPerson](isocialpersoniunknown.md) com base em que o parâmetro _userID_ .</span><span class="sxs-lookup"><span data-stu-id="225f4-104">Gets an [ISocialPerson](isocialpersoniunknown.md) interface based on the  _userID_ parameter.</span></span> 
  
```cpp
HRESULT _stdcall GetPerson([in] BSTR userId, [out, retval] ISocialPerson** result);
```

## <a name="parameters"></a><span data-ttu-id="225f4-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="225f4-105">Parameters</span></span>

<span data-ttu-id="225f4-106">_userId_</span><span class="sxs-lookup"><span data-stu-id="225f4-106">_userId_</span></span>
  
> <span data-ttu-id="225f4-107">[in] Uma cadeia de caracteres que contém um endereço SMTP ou de ID de usuário de uma pessoa.</span><span class="sxs-lookup"><span data-stu-id="225f4-107">[in] A string that contains a user ID or SMTP address of a person.</span></span>
    
<span data-ttu-id="225f4-108">_resultado_</span><span class="sxs-lookup"><span data-stu-id="225f4-108">_result_</span></span>
  
> <span data-ttu-id="225f4-109">[out] Uma interface **ISocialPerson** .</span><span class="sxs-lookup"><span data-stu-id="225f4-109">[out] An **ISocialPerson** interface.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="225f4-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="225f4-110">Remarks</span></span>

<span data-ttu-id="225f4-111">O parâmetro _userID_ deve ser um endereço SMTP ou de ID de usuário.</span><span class="sxs-lookup"><span data-stu-id="225f4-111">The  _userID_ parameter must be a user ID or SMTP address.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="225f4-112">Confira também</span><span class="sxs-lookup"><span data-stu-id="225f4-112">See also</span></span>

- [<span data-ttu-id="225f4-113">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="225f4-113">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)

