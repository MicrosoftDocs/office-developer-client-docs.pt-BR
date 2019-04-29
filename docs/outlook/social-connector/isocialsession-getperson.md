---
title: ISocialSessionGetPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2d0a2945-54d7-417f-b5c6-2647c70263cf
description: Obtém uma interface ISocialPerson com base no parâmetro userID.
ms.openlocfilehash: b54e39b3712fb57d89d03787f1e5fa0ff50ff84a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439818"
---
# <a name="isocialsessiongetperson"></a><span data-ttu-id="37623-103">ISocialSession::GetPerson</span><span class="sxs-lookup"><span data-stu-id="37623-103">ISocialSession::GetPerson</span></span>

<span data-ttu-id="37623-104">Obtém uma interface [ISocialPerson](isocialpersoniunknown.md) com base no parâmetro _userid_ .</span><span class="sxs-lookup"><span data-stu-id="37623-104">Gets an [ISocialPerson](isocialpersoniunknown.md) interface based on the  _userID_ parameter.</span></span> 
  
```cpp
HRESULT _stdcall GetPerson([in] BSTR userId, [out, retval] ISocialPerson** result);
```

## <a name="parameters"></a><span data-ttu-id="37623-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="37623-105">Parameters</span></span>

<span data-ttu-id="37623-106">_ID_</span><span class="sxs-lookup"><span data-stu-id="37623-106">_userId_</span></span>
  
> <span data-ttu-id="37623-107">no Uma cadeia de caracteres que contém uma ID de usuário ou endereço SMTP de uma pessoa.</span><span class="sxs-lookup"><span data-stu-id="37623-107">[in] A string that contains a user ID or SMTP address of a person.</span></span>
    
<span data-ttu-id="37623-108">_result_</span><span class="sxs-lookup"><span data-stu-id="37623-108">_result_</span></span>
  
> <span data-ttu-id="37623-109">bota Uma interface **ISocialPerson** .</span><span class="sxs-lookup"><span data-stu-id="37623-109">[out] An **ISocialPerson** interface.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="37623-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="37623-110">Remarks</span></span>

<span data-ttu-id="37623-111">O parâmetro _userid_ deve ser uma ID de usuário ou um endereço SMTP.</span><span class="sxs-lookup"><span data-stu-id="37623-111">The  _userID_ parameter must be a user ID or SMTP address.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="37623-112">Confira também</span><span class="sxs-lookup"><span data-stu-id="37623-112">See also</span></span>

- [<span data-ttu-id="37623-113">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="37623-113">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)

