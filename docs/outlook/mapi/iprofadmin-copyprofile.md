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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: cd70f5ee7b58bdf0b1fd61b1056bfc77e3e35992
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767614"
---
# <a name="iprofadmincopyprofile"></a><span data-ttu-id="5a880-103">IProfAdmin::CopyProfile</span><span class="sxs-lookup"><span data-stu-id="5a880-103">IProfAdmin::CopyProfile</span></span>

  
  
<span data-ttu-id="5a880-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5a880-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5a880-105">Copia um perfil.</span><span class="sxs-lookup"><span data-stu-id="5a880-105">Copies a profile.</span></span>
  
```cpp
HRESULTCopyProfile(
  LPSTR lpszOldProfileName,
  LPSTR lpszOldPassword,
  LPSTR lpszNewProfileName,
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="5a880-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5a880-106">Parameters</span></span>

 <span data-ttu-id="5a880-107">_lpszOldProfileName_</span><span class="sxs-lookup"><span data-stu-id="5a880-107">_lpszOldProfileName_</span></span>
  
> <span data-ttu-id="5a880-108">[in] Um ponteiro para o nome do perfil para copiar.</span><span class="sxs-lookup"><span data-stu-id="5a880-108">[in] A pointer to the name of the profile to copy.</span></span>
    
 <span data-ttu-id="5a880-109">_lpszOldPassword_</span><span class="sxs-lookup"><span data-stu-id="5a880-109">_lpszOldPassword_</span></span>
  
> <span data-ttu-id="5a880-110">[in] Um ponteiro para a senha do perfil para copiar.</span><span class="sxs-lookup"><span data-stu-id="5a880-110">[in] A pointer to the password of the profile to copy.</span></span>
    
 <span data-ttu-id="5a880-111">_lpszNewProfileName_</span><span class="sxs-lookup"><span data-stu-id="5a880-111">_lpszNewProfileName_</span></span>
  
> <span data-ttu-id="5a880-112">[in] Um ponteiro para o novo nome do perfil copiado.</span><span class="sxs-lookup"><span data-stu-id="5a880-112">[in] A pointer to the new name of the copied profile.</span></span>
    
 <span data-ttu-id="5a880-113">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="5a880-113">_ulUIParam_</span></span>
  
> <span data-ttu-id="5a880-114">[in] Um identificador para a janela pai de todas as caixas de diálogo ou windows que esse método exibe.</span><span class="sxs-lookup"><span data-stu-id="5a880-114">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span>
    
 <span data-ttu-id="5a880-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5a880-115">_ulFlags_</span></span>
  
> <span data-ttu-id="5a880-116">[in] Uma bitmask dos sinalizadores que controla como o perfil é copiado.</span><span class="sxs-lookup"><span data-stu-id="5a880-116">[in] A bitmask of flags that controls how the profile is copied.</span></span> <span data-ttu-id="5a880-117">Sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="5a880-117">The following flags can be set:</span></span>
    
<span data-ttu-id="5a880-118">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="5a880-118">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="5a880-119">Exibe uma caixa de diálogo que solicita ao usuário a senha correta do perfil para copiar.</span><span class="sxs-lookup"><span data-stu-id="5a880-119">Displays a dialog box that prompts the user for the correct password of the profile to copy.</span></span> <span data-ttu-id="5a880-120">Se esse sinalizador não estiver definida, nenhuma caixa de diálogo é exibida.</span><span class="sxs-lookup"><span data-stu-id="5a880-120">If this flag is not set, no dialog box is displayed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5a880-121">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="5a880-121">Return value</span></span>

<span data-ttu-id="5a880-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="5a880-122">S_OK</span></span> 
  
> <span data-ttu-id="5a880-123">O perfil foi copiado com êxito.</span><span class="sxs-lookup"><span data-stu-id="5a880-123">The profile was successfully copied.</span></span>
    
<span data-ttu-id="5a880-124">MAPI_E_ACCESS_DENIED</span><span class="sxs-lookup"><span data-stu-id="5a880-124">MAPI_E_ACCESS_DENIED</span></span> 
  
> <span data-ttu-id="5a880-125">O nome do novo perfil é igual de um perfil existente.</span><span class="sxs-lookup"><span data-stu-id="5a880-125">The new profile name is the same as that of an existing profile.</span></span>
    
<span data-ttu-id="5a880-126">MAPI_E_LOGON_FAILED</span><span class="sxs-lookup"><span data-stu-id="5a880-126">MAPI_E_LOGON_FAILED</span></span> 
  
> <span data-ttu-id="5a880-127">A senha para o perfil copiar estiver incorreta, e uma caixa de diálogo não pôde ser exibida para o usuário para solicitar a senha correta porque MAPI_DIALOG não foi definido no parâmetro _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="5a880-127">The password for the profile to copy is incorrect, and a dialog box could not be displayed to the user to request the correct password because MAPI_DIALOG was not set in the  _ulFlags_ parameter.</span></span> 
    
<span data-ttu-id="5a880-128">E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="5a880-128">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="5a880-129">O perfil especificado não existe.</span><span class="sxs-lookup"><span data-stu-id="5a880-129">The specified profile does not exist.</span></span>
    
<span data-ttu-id="5a880-130">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="5a880-130">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="5a880-131">O usuário cancelou a operação, geralmente clicando no botão **Cancelar** em uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="5a880-131">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="5a880-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="5a880-132">Remarks</span></span>

<span data-ttu-id="5a880-133">O método **IProfAdmin::CopyProfile** faz uma cópia do perfil apontado pela _lpszOldProfileName_, dando a ele o nome apontada pela _lpszNewProfileName_.</span><span class="sxs-lookup"><span data-stu-id="5a880-133">The **IProfAdmin::CopyProfile** method makes a copy of the profile pointed to by  _lpszOldProfileName_, giving it the name pointed to by  _lpszNewProfileName_.</span></span> <span data-ttu-id="5a880-134">Copiar um perfil deixa a cópia com a mesma senha que o original.</span><span class="sxs-lookup"><span data-stu-id="5a880-134">Copying a profile leaves the copy with the same password as the original.</span></span>
  
<span data-ttu-id="5a880-135">O nome do perfil original, sua senha e a cópia pode ter até 64 caracteres de comprimento e pode incluir os seguintes caracteres:</span><span class="sxs-lookup"><span data-stu-id="5a880-135">The name of the original profile, its password, and the copy can be up to 64 characters in length and can include the following characters:</span></span>
  
- <span data-ttu-id="5a880-136">Todos os caracteres alfanuméricos, incluindo o caractere de sublinhado e ênfase.</span><span class="sxs-lookup"><span data-stu-id="5a880-136">All alphanumeric characters, including accent characters and the underscore character.</span></span>
    
- <span data-ttu-id="5a880-137">Espaços incorporados, mas não espaços à esquerda ou à direita.</span><span class="sxs-lookup"><span data-stu-id="5a880-137">Embedded spaces, but not leading or trailing spaces.</span></span>
    
<span data-ttu-id="5a880-138">Senhas de perfil não são suportadas em todos os sistemas operacionais.</span><span class="sxs-lookup"><span data-stu-id="5a880-138">Profile passwords are not supported on all operating systems.</span></span> <span data-ttu-id="5a880-139">Nos sistemas operacionais que não oferecem suporte a senhas de perfil, _lpszOldPassword_ pode ser NULL ou um ponteiro para uma cadeia de caracteres de comprimento zero.</span><span class="sxs-lookup"><span data-stu-id="5a880-139">On operating systems that do not support profile passwords,  _lpszOldPassword_ can be NULL or a pointer to a zero-length string.</span></span> 
  
<span data-ttu-id="5a880-140">Se _lpszOldPassword_ for definido como NULL, o perfil a ser copiado exige uma senha e o sinalizador MAPI_DIALOG está definido; uma caixa de diálogo que solicita ao usuário para fornecer a senha é exibida.</span><span class="sxs-lookup"><span data-stu-id="5a880-140">If  _lpszOldPassword_ is set to NULL, the profile to be copied requires a password, and the MAPI_DIALOG flag is set; a dialog box that prompts the user to provide the password is displayed.</span></span> <span data-ttu-id="5a880-141">Se uma senha é exigida, mas _lpszOldPassword_ for definido como nulo e o sinalizador MAPI_DIALOG não estiver definido, **CopyProfile** retorna MAPI_E_LOGON_FAILED.</span><span class="sxs-lookup"><span data-stu-id="5a880-141">If a password is required, but  _lpszOldPassword_ is set to NULL and the MAPI_DIALOG flag is not set, **CopyProfile** returns MAPI_E_LOGON_FAILED.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5a880-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="5a880-142">See also</span></span>



[<span data-ttu-id="5a880-143">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5a880-143">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)

