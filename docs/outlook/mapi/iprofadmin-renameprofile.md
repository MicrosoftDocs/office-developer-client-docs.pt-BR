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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 162f20485fc21cf8523b6d4a653e52c35f4b3d9a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317077"
---
# <a name="iprofadminrenameprofile"></a><span data-ttu-id="d1f24-103">IProfAdmin::RenameProfile</span><span class="sxs-lookup"><span data-stu-id="d1f24-103">IProfAdmin::RenameProfile</span></span>

  
  
<span data-ttu-id="d1f24-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d1f24-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d1f24-105">Atribui um novo nome a um perfil.</span><span class="sxs-lookup"><span data-stu-id="d1f24-105">Assigns a new name to a profile.</span></span>
  
```cpp
HRESULT RenameProfile(
  LPSTR lpszOldProfileName,
  LPSTR lpszOldPassword,
  LPSTR lpszNewProfileName,
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="d1f24-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d1f24-106">Parameters</span></span>

 <span data-ttu-id="d1f24-107">_lpszOldProfileName_</span><span class="sxs-lookup"><span data-stu-id="d1f24-107">_lpszOldProfileName_</span></span>
  
> <span data-ttu-id="d1f24-108">no Um ponteiro para o nome atual do perfil a ser renomeado.</span><span class="sxs-lookup"><span data-stu-id="d1f24-108">[in] A pointer to the current name of the profile to rename.</span></span>
    
 <span data-ttu-id="d1f24-109">_lpszOldPassword_</span><span class="sxs-lookup"><span data-stu-id="d1f24-109">_lpszOldPassword_</span></span>
  
> <span data-ttu-id="d1f24-110">no Sempre nulo.</span><span class="sxs-lookup"><span data-stu-id="d1f24-110">[in] Always NULL.</span></span>
    
 <span data-ttu-id="d1f24-111">_lpszNewProfileName_</span><span class="sxs-lookup"><span data-stu-id="d1f24-111">_lpszNewProfileName_</span></span>
  
> <span data-ttu-id="d1f24-112">no Um ponteiro para o novo nome do perfil a ser renomeado.</span><span class="sxs-lookup"><span data-stu-id="d1f24-112">[in] A pointer to the new name of the profile to rename.</span></span>
    
 <span data-ttu-id="d1f24-113">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="d1f24-113">_ulUIParam_</span></span>
  
> <span data-ttu-id="d1f24-114">no Uma alça para a janela pai de quaisquer caixas de diálogo ou janelas que esse método exibe.</span><span class="sxs-lookup"><span data-stu-id="d1f24-114">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span> 
    
 <span data-ttu-id="d1f24-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d1f24-115">_ulFlags_</span></span>
  
> <span data-ttu-id="d1f24-116">no Sempre nulo.</span><span class="sxs-lookup"><span data-stu-id="d1f24-116">[in] Always NULL.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d1f24-117">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="d1f24-117">Return value</span></span>

<span data-ttu-id="d1f24-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="d1f24-118">S_OK</span></span> 
  
> <span data-ttu-id="d1f24-119">O perfil foi renomeado com êxito.</span><span class="sxs-lookup"><span data-stu-id="d1f24-119">The profile was successfully renamed.</span></span>
    
<span data-ttu-id="d1f24-120">MAPI_E_LOGON_FAILED</span><span class="sxs-lookup"><span data-stu-id="d1f24-120">MAPI_E_LOGON_FAILED</span></span> 
  
> <span data-ttu-id="d1f24-121">A senha do perfil está incorreta.</span><span class="sxs-lookup"><span data-stu-id="d1f24-121">The profile password is incorrect.</span></span>
    
<span data-ttu-id="d1f24-122">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="d1f24-122">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="d1f24-123">O usuário cancelou a operação, geralmente clicando no botão **Cancelar** em uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="d1f24-123">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="d1f24-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="d1f24-124">Remarks</span></span>

<span data-ttu-id="d1f24-125">O método **IProfAdmin:: RenameProfile** atribui um novo nome a um perfil, se ele tiver um.</span><span class="sxs-lookup"><span data-stu-id="d1f24-125">The **IProfAdmin::RenameProfile** method assigns a new name to a profile, if it has one.</span></span> <span data-ttu-id="d1f24-126">Se o perfil a ser renomeado estiver em uso por um cliente quando **RenameProfile** for chamado, o **RenameProfile** marcará o perfil e retornará S_OK em vez de tentar a operação de renomeação enquanto o perfil estiver em uso.</span><span class="sxs-lookup"><span data-stu-id="d1f24-126">If the profile to rename is in use by a client when **RenameProfile** is called, **RenameProfile** marks the profile and returns S_OK instead of attempting the rename operation while the profile is in use.</span></span> <span data-ttu-id="d1f24-127">Quando o perfil não está mais sendo usado, o **RenameProfile** atribui a ele o novo nome.</span><span class="sxs-lookup"><span data-stu-id="d1f24-127">When the profile is no longer being used, **RenameProfile** assigns it the new name.</span></span> 
  
<span data-ttu-id="d1f24-128">Os nomes antigo e novo do perfil podem ter até 64 caracteres de comprimento e podem incluir os seguintes caracteres:</span><span class="sxs-lookup"><span data-stu-id="d1f24-128">The old and new names of the profile can be up to 64 characters in length and can include the following characters:</span></span>
  
- <span data-ttu-id="d1f24-129">Todos os caracteres alfanuméricos, incluindo caracteres de ênfase e o caractere de sublinhado.</span><span class="sxs-lookup"><span data-stu-id="d1f24-129">All alphanumeric characters, including accent characters and the underscore character.</span></span>
    
- <span data-ttu-id="d1f24-130">Espaços incorporados, mas não espaços à esquerda ou à direita.</span><span class="sxs-lookup"><span data-stu-id="d1f24-130">Embedded spaces, but not leading or trailing spaces.</span></span>
    
<span data-ttu-id="d1f24-131">O _lpszPassword_ deve ser sempre nulo ou um ponteiro para uma sequência de comprimento zero.</span><span class="sxs-lookup"><span data-stu-id="d1f24-131">The  _lpszPassword_ should always be NULL or a pointer to a zero-length string.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d1f24-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="d1f24-132">See also</span></span>



[<span data-ttu-id="d1f24-133">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d1f24-133">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)

