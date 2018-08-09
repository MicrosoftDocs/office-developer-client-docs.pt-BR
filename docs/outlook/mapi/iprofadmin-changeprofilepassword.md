---
title: IProfAdminChangeProfilePassword
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.ChangeProfilePassword
api_type:
- COM
ms.assetid: a41f707a-5c84-49aa-aeb6-469b2600e181
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: c57f945d16cc80c637b1a4074b25f9cf1fb1edc0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767630"
---
# <a name="iprofadminchangeprofilepassword"></a><span data-ttu-id="3e11c-103">IProfAdmin::ChangeProfilePassword</span><span class="sxs-lookup"><span data-stu-id="3e11c-103">IProfAdmin::ChangeProfilePassword</span></span>

  
  
<span data-ttu-id="3e11c-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3e11c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3e11c-105">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="3e11c-105">Deprecated.</span></span> <span data-ttu-id="3e11c-106">Altera a senha de um perfil.</span><span class="sxs-lookup"><span data-stu-id="3e11c-106">Changes the password for a profile.</span></span>
  
```cpp
HRESULT ChangeProfilePassword(
  LPSTR lpszProfileName,
  LPSTR lpszOldPassword,
  LPSTR lpszNewPassword,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="3e11c-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3e11c-107">Parameters</span></span>

 <span data-ttu-id="3e11c-108">_lpszProfileName_</span><span class="sxs-lookup"><span data-stu-id="3e11c-108">_lpszProfileName_</span></span>
  
> <span data-ttu-id="3e11c-109">[in] Um ponteiro para o nome do perfil associado a senha a ser alterado.</span><span class="sxs-lookup"><span data-stu-id="3e11c-109">[in] A pointer to the name of the profile associated with the password to be changed.</span></span>
    
 <span data-ttu-id="3e11c-110">_lpszOldPassword_</span><span class="sxs-lookup"><span data-stu-id="3e11c-110">_lpszOldPassword_</span></span>
  
> <span data-ttu-id="3e11c-111">[in] Um ponteiro para a senha atual.</span><span class="sxs-lookup"><span data-stu-id="3e11c-111">[in] A pointer to the current password.</span></span>
    
 <span data-ttu-id="3e11c-112">_lpszNewPassword_</span><span class="sxs-lookup"><span data-stu-id="3e11c-112">_lpszNewPassword_</span></span>
  
> <span data-ttu-id="3e11c-113">[in] Um ponteiro para a nova senha.</span><span class="sxs-lookup"><span data-stu-id="3e11c-113">[in] A pointer to the new password.</span></span>
    
 <span data-ttu-id="3e11c-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="3e11c-114">_ulFlags_</span></span>
  
> <span data-ttu-id="3e11c-115">[in] Uma bitmask dos sinalizadores que controla o tipo das cadeias de caracteres no passado.</span><span class="sxs-lookup"><span data-stu-id="3e11c-115">[in] A bitmask of flags that controls the type of the passed-in strings.</span></span> <span data-ttu-id="3e11c-116">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="3e11c-116">The following flag can be set:</span></span>
    
<span data-ttu-id="3e11c-117">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="3e11c-117">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="3e11c-118">O nome do perfil e senhas estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="3e11c-118">The profile name and passwords are in Unicode format.</span></span> <span data-ttu-id="3e11c-119">Se o sinalizador MAPI_UNICODE não estiver definido, essas cadeias de caracteres estão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="3e11c-119">If the MAPI_UNICODE flag is not set, these strings are in ANSI format.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="3e11c-120">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="3e11c-120">Return value</span></span>

<span data-ttu-id="3e11c-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="3e11c-121">S_OK</span></span> 
  
> <span data-ttu-id="3e11c-122">Se esse método for chamado, ela retornará S_OK.</span><span class="sxs-lookup"><span data-stu-id="3e11c-122">If this method is called, it will return S_OK.</span></span> <span data-ttu-id="3e11c-123">No entanto, nenhuma ação será tomada.</span><span class="sxs-lookup"><span data-stu-id="3e11c-123">However, no action will be taken.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3e11c-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="3e11c-124">Remarks</span></span>

<span data-ttu-id="3e11c-125">Não use esse método.</span><span class="sxs-lookup"><span data-stu-id="3e11c-125">Do not use this method.</span></span> <span data-ttu-id="3e11c-126">MAPI não suporta senhas para perfis.</span><span class="sxs-lookup"><span data-stu-id="3e11c-126">MAPI does not support passwords for profiles.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="3e11c-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="3e11c-127">See also</span></span>



[<span data-ttu-id="3e11c-128">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3e11c-128">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)

