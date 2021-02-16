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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: c7124c8e3f2ced66d303321ff7aee8592a723a2b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420238"
---
# <a name="iprofadminchangeprofilepassword"></a><span data-ttu-id="4d19a-103">IProfAdmin::ChangeProfilePassword</span><span class="sxs-lookup"><span data-stu-id="4d19a-103">IProfAdmin::ChangeProfilePassword</span></span>

  
  
<span data-ttu-id="4d19a-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4d19a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4d19a-105">Depreciado.</span><span class="sxs-lookup"><span data-stu-id="4d19a-105">Deprecated.</span></span> <span data-ttu-id="4d19a-106">Altera a senha de um perfil.</span><span class="sxs-lookup"><span data-stu-id="4d19a-106">Changes the password for a profile.</span></span>
  
```cpp
HRESULT ChangeProfilePassword(
  LPSTR lpszProfileName,
  LPSTR lpszOldPassword,
  LPSTR lpszNewPassword,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="4d19a-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4d19a-107">Parameters</span></span>

 <span data-ttu-id="4d19a-108">_lpszProfileName_</span><span class="sxs-lookup"><span data-stu-id="4d19a-108">_lpszProfileName_</span></span>
  
> <span data-ttu-id="4d19a-109">[in] Um ponteiro para o nome do perfil associado à senha a ser alterada.</span><span class="sxs-lookup"><span data-stu-id="4d19a-109">[in] A pointer to the name of the profile associated with the password to be changed.</span></span>
    
 <span data-ttu-id="4d19a-110">_lpszOldPassword_</span><span class="sxs-lookup"><span data-stu-id="4d19a-110">_lpszOldPassword_</span></span>
  
> <span data-ttu-id="4d19a-111">[in] Um ponteiro para a senha atual.</span><span class="sxs-lookup"><span data-stu-id="4d19a-111">[in] A pointer to the current password.</span></span>
    
 <span data-ttu-id="4d19a-112">_lpszNewPassword_</span><span class="sxs-lookup"><span data-stu-id="4d19a-112">_lpszNewPassword_</span></span>
  
> <span data-ttu-id="4d19a-113">[in] Um ponteiro para a nova senha.</span><span class="sxs-lookup"><span data-stu-id="4d19a-113">[in] A pointer to the new password.</span></span>
    
 <span data-ttu-id="4d19a-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4d19a-114">_ulFlags_</span></span>
  
> <span data-ttu-id="4d19a-115">[in] Uma máscara de bits de sinalizadores que controla o tipo das cadeias de caracteres passadas.</span><span class="sxs-lookup"><span data-stu-id="4d19a-115">[in] A bitmask of flags that controls the type of the passed-in strings.</span></span> <span data-ttu-id="4d19a-116">O sinalizador a seguir pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="4d19a-116">The following flag can be set:</span></span>
    
<span data-ttu-id="4d19a-117">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="4d19a-117">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="4d19a-118">O nome do perfil e as senhas estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="4d19a-118">The profile name and passwords are in Unicode format.</span></span> <span data-ttu-id="4d19a-119">Se o MAPI_UNICODE não estiver definido, essas cadeias de caracteres estão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="4d19a-119">If the MAPI_UNICODE flag is not set, these strings are in ANSI format.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4d19a-120">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="4d19a-120">Return value</span></span>

<span data-ttu-id="4d19a-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="4d19a-121">S_OK</span></span> 
  
> <span data-ttu-id="4d19a-122">Se esse método for chamado, ele retornará S_OK.</span><span class="sxs-lookup"><span data-stu-id="4d19a-122">If this method is called, it will return S_OK.</span></span> <span data-ttu-id="4d19a-123">No entanto, nenhuma ação será tomada.</span><span class="sxs-lookup"><span data-stu-id="4d19a-123">However, no action will be taken.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4d19a-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="4d19a-124">Remarks</span></span>

<span data-ttu-id="4d19a-125">Não use esse método.</span><span class="sxs-lookup"><span data-stu-id="4d19a-125">Do not use this method.</span></span> <span data-ttu-id="4d19a-126">O MAPI não dá suporte a senhas para perfis.</span><span class="sxs-lookup"><span data-stu-id="4d19a-126">MAPI does not support passwords for profiles.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4d19a-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="4d19a-127">See also</span></span>



[<span data-ttu-id="4d19a-128">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4d19a-128">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)

