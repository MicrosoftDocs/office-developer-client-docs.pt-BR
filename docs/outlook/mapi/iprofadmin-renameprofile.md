---
title: IProfAdminRenameProfile
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.RenameProfile
api_type:
- COM
ms.assetid: 2a575cac-dbfd-4f42-9c10-4b7e355a065e
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: c94c60cf9ff1adbe2b54bd85b228e21b4be0e6e1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767625"
---
# <a name="iprofadminrenameprofile"></a><span data-ttu-id="c26be-103">IProfAdmin::RenameProfile</span><span class="sxs-lookup"><span data-stu-id="c26be-103">IProfAdmin::RenameProfile</span></span>

  
  
<span data-ttu-id="c26be-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c26be-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c26be-105">Atribui um novo nome a um perfil.</span><span class="sxs-lookup"><span data-stu-id="c26be-105">Assigns a new name to a profile.</span></span>
  
```cpp
HRESULT RenameProfile(
  LPSTR lpszOldProfileName,
  LPSTR lpszOldPassword,
  LPSTR lpszNewProfileName,
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="c26be-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="c26be-106">Parameters</span></span>

 <span data-ttu-id="c26be-107">_lpszOldProfileName_</span><span class="sxs-lookup"><span data-stu-id="c26be-107">_lpszOldProfileName_</span></span>
  
> <span data-ttu-id="c26be-108">[in] Um ponteiro para o nome atual do perfil para renomear.</span><span class="sxs-lookup"><span data-stu-id="c26be-108">[in] A pointer to the current name of the profile to rename.</span></span>
    
 <span data-ttu-id="c26be-109">_lpszOldPassword_</span><span class="sxs-lookup"><span data-stu-id="c26be-109">_lpszOldPassword_</span></span>
  
> <span data-ttu-id="c26be-110">[in] Sempre nulo.</span><span class="sxs-lookup"><span data-stu-id="c26be-110">[in] Always NULL.</span></span>
    
 <span data-ttu-id="c26be-111">_lpszNewProfileName_</span><span class="sxs-lookup"><span data-stu-id="c26be-111">_lpszNewProfileName_</span></span>
  
> <span data-ttu-id="c26be-112">[in] Um ponteiro para o novo nome do perfil para renomear.</span><span class="sxs-lookup"><span data-stu-id="c26be-112">[in] A pointer to the new name of the profile to rename.</span></span>
    
 <span data-ttu-id="c26be-113">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="c26be-113">_ulUIParam_</span></span>
  
> <span data-ttu-id="c26be-114">[in] Um identificador para a janela pai de todas as caixas de diálogo ou windows que esse método exibe.</span><span class="sxs-lookup"><span data-stu-id="c26be-114">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span> 
    
 <span data-ttu-id="c26be-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c26be-115">_ulFlags_</span></span>
  
> <span data-ttu-id="c26be-116">[in] Sempre nulo.</span><span class="sxs-lookup"><span data-stu-id="c26be-116">[in] Always NULL.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c26be-117">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="c26be-117">Return value</span></span>

<span data-ttu-id="c26be-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="c26be-118">S_OK</span></span> 
  
> <span data-ttu-id="c26be-119">O perfil foi renomeado com êxito.</span><span class="sxs-lookup"><span data-stu-id="c26be-119">The profile was successfully renamed.</span></span>
    
<span data-ttu-id="c26be-120">MAPI_E_LOGON_FAILED</span><span class="sxs-lookup"><span data-stu-id="c26be-120">MAPI_E_LOGON_FAILED</span></span> 
  
> <span data-ttu-id="c26be-121">A senha do perfil está incorreta.</span><span class="sxs-lookup"><span data-stu-id="c26be-121">The profile password is incorrect.</span></span>
    
<span data-ttu-id="c26be-122">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="c26be-122">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="c26be-123">O usuário cancelou a operação, geralmente clicando no botão **Cancelar** em uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="c26be-123">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="c26be-124">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="c26be-124">Remarks</span></span>

<span data-ttu-id="c26be-125">O método **IProfAdmin::RenameProfile** atribui um novo nome para um perfil, caso haja algum.</span><span class="sxs-lookup"><span data-stu-id="c26be-125">The **IProfAdmin::RenameProfile** method assigns a new name to a profile, if it has one.</span></span> <span data-ttu-id="c26be-126">Se o perfil renomear estiver sendo usado por um cliente quando **RenameProfile** é chamado, o **RenameProfile** marca o perfil e retorna S_OK em vez de tentar a operação de renomeação enquanto o perfil estiver em uso.</span><span class="sxs-lookup"><span data-stu-id="c26be-126">If the profile to rename is in use by a client when **RenameProfile** is called, **RenameProfile** marks the profile and returns S_OK instead of attempting the rename operation while the profile is in use.</span></span> <span data-ttu-id="c26be-127">Quando o perfil não mais estiver sendo usado, **RenameProfile** atribui o novo nome.</span><span class="sxs-lookup"><span data-stu-id="c26be-127">When the profile is no longer being used, **RenameProfile** assigns it the new name.</span></span> 
  
<span data-ttu-id="c26be-128">Os nomes antigos e novos do perfil podem ter até 64 caracteres de comprimento e podem incluir os seguintes caracteres:</span><span class="sxs-lookup"><span data-stu-id="c26be-128">The old and new names of the profile can be up to 64 characters in length and can include the following characters:</span></span>
  
- <span data-ttu-id="c26be-129">Todos os caracteres alfanuméricos, incluindo o caractere de sublinhado e ênfase.</span><span class="sxs-lookup"><span data-stu-id="c26be-129">All alphanumeric characters, including accent characters and the underscore character.</span></span>
    
- <span data-ttu-id="c26be-130">Espaços incorporados, mas não espaços à esquerda ou à direita.</span><span class="sxs-lookup"><span data-stu-id="c26be-130">Embedded spaces, but not leading or trailing spaces.</span></span>
    
<span data-ttu-id="c26be-131">O _lpszPassword_ deve sempre ser NULL ou um ponteiro para uma cadeia de caracteres de comprimento zero.</span><span class="sxs-lookup"><span data-stu-id="c26be-131">The  _lpszPassword_ should always be NULL or a pointer to a zero-length string.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c26be-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="c26be-132">See also</span></span>



[<span data-ttu-id="c26be-133">IProfAdmin: IUnknown</span><span class="sxs-lookup"><span data-stu-id="c26be-133">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)

