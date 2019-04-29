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
# <a name="iprofadmincopyprofile"></a><span data-ttu-id="a4b84-103">IProfAdmin::CopyProfile</span><span class="sxs-lookup"><span data-stu-id="a4b84-103">IProfAdmin::CopyProfile</span></span>

  
  
<span data-ttu-id="a4b84-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a4b84-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a4b84-105">Copia um perfil.</span><span class="sxs-lookup"><span data-stu-id="a4b84-105">Copies a profile.</span></span>
  
```cpp
HRESULTCopyProfile(
  LPSTR lpszOldProfileName,
  LPSTR lpszOldPassword,
  LPSTR lpszNewProfileName,
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="a4b84-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a4b84-106">Parameters</span></span>

 <span data-ttu-id="a4b84-107">_lpszOldProfileName_</span><span class="sxs-lookup"><span data-stu-id="a4b84-107">_lpszOldProfileName_</span></span>
  
> <span data-ttu-id="a4b84-108">no Um ponteiro para o nome do perfil a ser copiado.</span><span class="sxs-lookup"><span data-stu-id="a4b84-108">[in] A pointer to the name of the profile to copy.</span></span>
    
 <span data-ttu-id="a4b84-109">_lpszOldPassword_</span><span class="sxs-lookup"><span data-stu-id="a4b84-109">_lpszOldPassword_</span></span>
  
> <span data-ttu-id="a4b84-110">no Um ponteiro para a senha do perfil a ser copiado.</span><span class="sxs-lookup"><span data-stu-id="a4b84-110">[in] A pointer to the password of the profile to copy.</span></span>
    
 <span data-ttu-id="a4b84-111">_lpszNewProfileName_</span><span class="sxs-lookup"><span data-stu-id="a4b84-111">_lpszNewProfileName_</span></span>
  
> <span data-ttu-id="a4b84-112">no Um ponteiro para o novo nome do perfil copiado.</span><span class="sxs-lookup"><span data-stu-id="a4b84-112">[in] A pointer to the new name of the copied profile.</span></span>
    
 <span data-ttu-id="a4b84-113">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="a4b84-113">_ulUIParam_</span></span>
  
> <span data-ttu-id="a4b84-114">no Uma alça para a janela pai de quaisquer caixas de diálogo ou janelas que esse método exibe.</span><span class="sxs-lookup"><span data-stu-id="a4b84-114">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span>
    
 <span data-ttu-id="a4b84-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a4b84-115">_ulFlags_</span></span>
  
> <span data-ttu-id="a4b84-116">no Uma bitmask de sinalizadores que controla como o perfil é copiado.</span><span class="sxs-lookup"><span data-stu-id="a4b84-116">[in] A bitmask of flags that controls how the profile is copied.</span></span> <span data-ttu-id="a4b84-117">Os seguintes sinalizadores podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="a4b84-117">The following flags can be set:</span></span>
    
<span data-ttu-id="a4b84-118">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="a4b84-118">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="a4b84-119">Exibe uma caixa de diálogo que solicita ao usuário a senha correta do perfil a ser copiado.</span><span class="sxs-lookup"><span data-stu-id="a4b84-119">Displays a dialog box that prompts the user for the correct password of the profile to copy.</span></span> <span data-ttu-id="a4b84-120">Se esse sinalizador não for definido, nenhuma caixa de diálogo será exibida.</span><span class="sxs-lookup"><span data-stu-id="a4b84-120">If this flag is not set, no dialog box is displayed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a4b84-121">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="a4b84-121">Return value</span></span>

<span data-ttu-id="a4b84-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="a4b84-122">S_OK</span></span> 
  
> <span data-ttu-id="a4b84-123">O perfil foi copiado com êxito.</span><span class="sxs-lookup"><span data-stu-id="a4b84-123">The profile was successfully copied.</span></span>
    
<span data-ttu-id="a4b84-124">MAPI_E_ACCESS_DENIED</span><span class="sxs-lookup"><span data-stu-id="a4b84-124">MAPI_E_ACCESS_DENIED</span></span> 
  
> <span data-ttu-id="a4b84-125">O novo nome do perfil é o mesmo de um perfil existente.</span><span class="sxs-lookup"><span data-stu-id="a4b84-125">The new profile name is the same as that of an existing profile.</span></span>
    
<span data-ttu-id="a4b84-126">MAPI_E_LOGON_FAILED</span><span class="sxs-lookup"><span data-stu-id="a4b84-126">MAPI_E_LOGON_FAILED</span></span> 
  
> <span data-ttu-id="a4b84-127">A senha do perfil a ser copiada está incorreta e uma caixa de diálogo não pôde ser exibida para o usuário solicitar a senha correta porque MAPI_DIALOG não foi definido no parâmetro _parâmetroulflags_ .</span><span class="sxs-lookup"><span data-stu-id="a4b84-127">The password for the profile to copy is incorrect, and a dialog box could not be displayed to the user to request the correct password because MAPI_DIALOG was not set in the  _ulFlags_ parameter.</span></span> 
    
<span data-ttu-id="a4b84-128">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="a4b84-128">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="a4b84-129">O perfil especificado não existe.</span><span class="sxs-lookup"><span data-stu-id="a4b84-129">The specified profile does not exist.</span></span>
    
<span data-ttu-id="a4b84-130">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="a4b84-130">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="a4b84-131">O usuário cancelou a operação, geralmente clicando no botão **Cancelar** em uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="a4b84-131">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="a4b84-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="a4b84-132">Remarks</span></span>

<span data-ttu-id="a4b84-133">O método **IProfAdmin:: CopyProfile** faz uma cópia do perfil apontada pelo _lpszOldProfileName_, dando a ele o nome apontado por _lpszNewProfileName_.</span><span class="sxs-lookup"><span data-stu-id="a4b84-133">The **IProfAdmin::CopyProfile** method makes a copy of the profile pointed to by  _lpszOldProfileName_, giving it the name pointed to by  _lpszNewProfileName_.</span></span> <span data-ttu-id="a4b84-134">Copiar um perfil deixa a cópia com a mesma senha que o original.</span><span class="sxs-lookup"><span data-stu-id="a4b84-134">Copying a profile leaves the copy with the same password as the original.</span></span>
  
<span data-ttu-id="a4b84-135">O nome do perfil original, sua senha e a cópia podem ter até 64 caracteres de comprimento e podem incluir os seguintes caracteres:</span><span class="sxs-lookup"><span data-stu-id="a4b84-135">The name of the original profile, its password, and the copy can be up to 64 characters in length and can include the following characters:</span></span>
  
- <span data-ttu-id="a4b84-136">Todos os caracteres alfanuméricos, incluindo caracteres de ênfase e o caractere de sublinhado.</span><span class="sxs-lookup"><span data-stu-id="a4b84-136">All alphanumeric characters, including accent characters and the underscore character.</span></span>
    
- <span data-ttu-id="a4b84-137">Espaços incorporados, mas não espaços à esquerda ou à direita.</span><span class="sxs-lookup"><span data-stu-id="a4b84-137">Embedded spaces, but not leading or trailing spaces.</span></span>
    
<span data-ttu-id="a4b84-138">As senhas de perfil não são suportadas em todos os sistemas operacionais.</span><span class="sxs-lookup"><span data-stu-id="a4b84-138">Profile passwords are not supported on all operating systems.</span></span> <span data-ttu-id="a4b84-139">Em sistemas operacionais que não dão suporte a senhas de perfil, _lpszOldPassword_ pode ser NULL ou um ponteiro para uma sequência de comprimento zero.</span><span class="sxs-lookup"><span data-stu-id="a4b84-139">On operating systems that do not support profile passwords,  _lpszOldPassword_ can be NULL or a pointer to a zero-length string.</span></span> 
  
<span data-ttu-id="a4b84-140">Se _lpszOldPassword_ estiver definido como nulo, o perfil a ser copiado requer uma senha e o sinalizador MAPI_DIALOG é definido; é exibida uma caixa de diálogo solicitando que o usuário forneça a senha.</span><span class="sxs-lookup"><span data-stu-id="a4b84-140">If  _lpszOldPassword_ is set to NULL, the profile to be copied requires a password, and the MAPI_DIALOG flag is set; a dialog box that prompts the user to provide the password is displayed.</span></span> <span data-ttu-id="a4b84-141">Se uma senha for necessária, mas _lpszOldPassword_ estiver definida como nulo e o sinalizador MAPI_DIALOG não estiver definido, **CopyProfile** retornará MAPI_E_LOGON_FAILED.</span><span class="sxs-lookup"><span data-stu-id="a4b84-141">If a password is required, but  _lpszOldPassword_ is set to NULL and the MAPI_DIALOG flag is not set, **CopyProfile** returns MAPI_E_LOGON_FAILED.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a4b84-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="a4b84-142">See also</span></span>



[<span data-ttu-id="a4b84-143">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a4b84-143">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)

