---
title: IProfAdminCopyProfile
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.CopyProfile
api_type:
- COM
ms.assetid: f4846dc3-0236-44ed-a1b1-8c13d48fb58a
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: c3c4ac10003aad8949de94e0f144410af10078b1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437235"
---
# <a name="iprofadmincopyprofile"></a><span data-ttu-id="7d998-103">IProfAdmin::CopyProfile</span><span class="sxs-lookup"><span data-stu-id="7d998-103">IProfAdmin::CopyProfile</span></span>

  
  
<span data-ttu-id="7d998-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7d998-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7d998-105">Copia um perfil.</span><span class="sxs-lookup"><span data-stu-id="7d998-105">Copies a profile.</span></span>
  
```cpp
HRESULTCopyProfile(
  LPSTR lpszOldProfileName,
  LPSTR lpszOldPassword,
  LPSTR lpszNewProfileName,
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="7d998-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7d998-106">Parameters</span></span>

 <span data-ttu-id="7d998-107">_lpszOldProfileName_</span><span class="sxs-lookup"><span data-stu-id="7d998-107">_lpszOldProfileName_</span></span>
  
> <span data-ttu-id="7d998-108">[in] Um ponteiro para o nome do perfil a ser copiado.</span><span class="sxs-lookup"><span data-stu-id="7d998-108">[in] A pointer to the name of the profile to copy.</span></span>
    
 <span data-ttu-id="7d998-109">_lpszOldPassword_</span><span class="sxs-lookup"><span data-stu-id="7d998-109">_lpszOldPassword_</span></span>
  
> <span data-ttu-id="7d998-110">[in] Um ponteiro para a senha do perfil a ser copiado.</span><span class="sxs-lookup"><span data-stu-id="7d998-110">[in] A pointer to the password of the profile to copy.</span></span>
    
 <span data-ttu-id="7d998-111">_lpszNewProfileName_</span><span class="sxs-lookup"><span data-stu-id="7d998-111">_lpszNewProfileName_</span></span>
  
> <span data-ttu-id="7d998-112">[in] Um ponteiro para o novo nome do perfil copiado.</span><span class="sxs-lookup"><span data-stu-id="7d998-112">[in] A pointer to the new name of the copied profile.</span></span>
    
 <span data-ttu-id="7d998-113">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="7d998-113">_ulUIParam_</span></span>
  
> <span data-ttu-id="7d998-114">[in] Um alça para a janela pai de quaisquer caixas de diálogo ou janelas que esse método exibe.</span><span class="sxs-lookup"><span data-stu-id="7d998-114">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span>
    
 <span data-ttu-id="7d998-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="7d998-115">_ulFlags_</span></span>
  
> <span data-ttu-id="7d998-116">[in] Uma máscara de bits de sinalizadores que controla como o perfil é copiado.</span><span class="sxs-lookup"><span data-stu-id="7d998-116">[in] A bitmask of flags that controls how the profile is copied.</span></span> <span data-ttu-id="7d998-117">Os sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="7d998-117">The following flags can be set:</span></span>
    
<span data-ttu-id="7d998-118">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="7d998-118">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="7d998-119">Exibe uma caixa de diálogo que solicita ao usuário a senha correta do perfil a ser copiado.</span><span class="sxs-lookup"><span data-stu-id="7d998-119">Displays a dialog box that prompts the user for the correct password of the profile to copy.</span></span> <span data-ttu-id="7d998-120">Se esse sinalizador não estiver definido, nenhuma caixa de diálogo será exibida.</span><span class="sxs-lookup"><span data-stu-id="7d998-120">If this flag is not set, no dialog box is displayed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7d998-121">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="7d998-121">Return value</span></span>

<span data-ttu-id="7d998-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="7d998-122">S_OK</span></span> 
  
> <span data-ttu-id="7d998-123">O perfil foi copiado com êxito.</span><span class="sxs-lookup"><span data-stu-id="7d998-123">The profile was successfully copied.</span></span>
    
<span data-ttu-id="7d998-124">MAPI_E_ACCESS_DENIED</span><span class="sxs-lookup"><span data-stu-id="7d998-124">MAPI_E_ACCESS_DENIED</span></span> 
  
> <span data-ttu-id="7d998-125">O novo nome de perfil é o mesmo de um perfil existente.</span><span class="sxs-lookup"><span data-stu-id="7d998-125">The new profile name is the same as that of an existing profile.</span></span>
    
<span data-ttu-id="7d998-126">MAPI_E_LOGON_FAILED</span><span class="sxs-lookup"><span data-stu-id="7d998-126">MAPI_E_LOGON_FAILED</span></span> 
  
> <span data-ttu-id="7d998-127">A senha para o perfil a ser copiado está incorreta e uma caixa de diálogo não pôde ser exibida para o usuário para solicitar a senha correta porque MAPI_DIALOG não foi definido no _parâmetro ulFlags._</span><span class="sxs-lookup"><span data-stu-id="7d998-127">The password for the profile to copy is incorrect, and a dialog box could not be displayed to the user to request the correct password because MAPI_DIALOG was not set in the  _ulFlags_ parameter.</span></span> 
    
<span data-ttu-id="7d998-128">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="7d998-128">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="7d998-129">O perfil especificado não existe.</span><span class="sxs-lookup"><span data-stu-id="7d998-129">The specified profile does not exist.</span></span>
    
<span data-ttu-id="7d998-130">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="7d998-130">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="7d998-131">O usuário cancelou a operação, normalmente clicando no botão Cancelar **em** uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="7d998-131">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="7d998-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="7d998-132">Remarks</span></span>

<span data-ttu-id="7d998-133">O **método IProfAdmin::CopyProfile** faz uma cópia do perfil apontado por  _lpszOldProfileName_, dando a ele o nome apontado por  _lpszNewProfileName_.</span><span class="sxs-lookup"><span data-stu-id="7d998-133">The **IProfAdmin::CopyProfile** method makes a copy of the profile pointed to by  _lpszOldProfileName_, giving it the name pointed to by  _lpszNewProfileName_.</span></span> <span data-ttu-id="7d998-134">Copiar um perfil deixa a cópia com a mesma senha do original.</span><span class="sxs-lookup"><span data-stu-id="7d998-134">Copying a profile leaves the copy with the same password as the original.</span></span>
  
<span data-ttu-id="7d998-135">O nome do perfil original, sua senha e a cópia podem ter até 64 caracteres e podem incluir os seguintes caracteres:</span><span class="sxs-lookup"><span data-stu-id="7d998-135">The name of the original profile, its password, and the copy can be up to 64 characters in length and can include the following characters:</span></span>
  
- <span data-ttu-id="7d998-136">Todos os caracteres alfanuméricos, incluindo caracteres de ênfase e o caractere de sublinhado.</span><span class="sxs-lookup"><span data-stu-id="7d998-136">All alphanumeric characters, including accent characters and the underscore character.</span></span>
    
- <span data-ttu-id="7d998-137">Espaços incorporados, mas não espaços à frente ou à frente.</span><span class="sxs-lookup"><span data-stu-id="7d998-137">Embedded spaces, but not leading or trailing spaces.</span></span>
    
<span data-ttu-id="7d998-138">Não há suporte para senhas de perfil em todos os sistemas operacionais.</span><span class="sxs-lookup"><span data-stu-id="7d998-138">Profile passwords are not supported on all operating systems.</span></span> <span data-ttu-id="7d998-139">Em sistemas operacionais que não suportam senhas de perfil,  _lpszOldPassword_ pode ser NULL ou um ponteiro para uma cadeia de caracteres de comprimento zero.</span><span class="sxs-lookup"><span data-stu-id="7d998-139">On operating systems that do not support profile passwords,  _lpszOldPassword_ can be NULL or a pointer to a zero-length string.</span></span> 
  
<span data-ttu-id="7d998-140">Se  _lpszOldPassword_ for definido como NULL, o perfil a ser copiado exigirá uma senha e o sinalizador MAPI_DIALOG definido; uma caixa de diálogo que solicita que o usuário forneça a senha é exibida.</span><span class="sxs-lookup"><span data-stu-id="7d998-140">If  _lpszOldPassword_ is set to NULL, the profile to be copied requires a password, and the MAPI_DIALOG flag is set; a dialog box that prompts the user to provide the password is displayed.</span></span> <span data-ttu-id="7d998-141">Se uma senha for necessária, mas  _lpszOldPassword_ for definida como NULL e o sinalizador MAPI_DIALOG não estiver definido, **CopyProfile** retornará MAPI_E_LOGON_FAILED.</span><span class="sxs-lookup"><span data-stu-id="7d998-141">If a password is required, but  _lpszOldPassword_ is set to NULL and the MAPI_DIALOG flag is not set, **CopyProfile** returns MAPI_E_LOGON_FAILED.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7d998-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="7d998-142">See also</span></span>



[<span data-ttu-id="7d998-143">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7d998-143">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)

