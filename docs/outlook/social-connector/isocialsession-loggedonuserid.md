---
title: ISocialSessionLoggedOnUserID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 54377ab4-8c69-4d7a-b9b7-278241823c8d
description: Retorna uma cadeia de caracteres que representa a ID de usuário da rede social do usuário conectado no momento.
ms.openlocfilehash: edb61569829f7690c2284a083d2cbd5cfe2d32a8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285279"
---
# <a name="isocialsessionloggedonuserid"></a><span data-ttu-id="7b447-103">ISocialSession::LoggedOnUserID</span><span class="sxs-lookup"><span data-stu-id="7b447-103">ISocialSession::LoggedOnUserID</span></span>

<span data-ttu-id="7b447-104">Retorna uma cadeia de caracteres que representa a ID de usuário da rede social do usuário conectado no momento.</span><span class="sxs-lookup"><span data-stu-id="7b447-104">Returns a string that represents the social network user ID of the user who is currently logged on.</span></span> 
  
```cpp
[propget] HRESULT _stdcall LoggedOnUserID([out, retval] BSTR* result);
```

## <a name="property-value"></a><span data-ttu-id="7b447-105">Valor de propriedade</span><span class="sxs-lookup"><span data-stu-id="7b447-105">Property value</span></span>

<span data-ttu-id="7b447-106">Uma cadeia de caracteres que contém a ID de usuário da rede social do usuário conectado.</span><span class="sxs-lookup"><span data-stu-id="7b447-106">A string that contains the social network user ID of the logged-on user.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7b447-107">Confira também</span><span class="sxs-lookup"><span data-stu-id="7b447-107">See also</span></span>

- [<span data-ttu-id="7b447-108">ISocialSession::LoggedOnUserName</span><span class="sxs-lookup"><span data-stu-id="7b447-108">ISocialSession::LoggedOnUserName</span></span>](isocialsession-loggedonusername.md)  
- [<span data-ttu-id="7b447-109">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7b447-109">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)

