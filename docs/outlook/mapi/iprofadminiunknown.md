---
title: IProfAdmin IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin
api_type:
- COM
ms.assetid: 274899cc-2894-4d99-84ec-f18121e856a0
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: c6192e6f92078f2f9bab0d55e9952d21ebb82af6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767628"
---
# <a name="iprofadmin--iunknown"></a><span data-ttu-id="55ebb-103">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="55ebb-103">IProfAdmin : IUnknown</span></span>

  
  
<span data-ttu-id="55ebb-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="55ebb-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="55ebb-105">Oferece suporte a administração de perfis.</span><span class="sxs-lookup"><span data-stu-id="55ebb-105">Supports the administration of profiles.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="55ebb-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="55ebb-106">Header file:</span></span>  <br/> |<span data-ttu-id="55ebb-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="55ebb-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="55ebb-108">Expostos pelo:</span><span class="sxs-lookup"><span data-stu-id="55ebb-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="55ebb-109">Objeto de administração de perfil</span><span class="sxs-lookup"><span data-stu-id="55ebb-109">Profile administration object</span></span>  <br/> |
|<span data-ttu-id="55ebb-110">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="55ebb-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="55ebb-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="55ebb-111">MAPI</span></span>  <br/> |
|<span data-ttu-id="55ebb-112">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="55ebb-112">Called by:</span></span>  <br/> |<span data-ttu-id="55ebb-113">Aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="55ebb-113">Client applications</span></span>  <br/> |
|<span data-ttu-id="55ebb-114">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="55ebb-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="55ebb-115">IID_IProfAdmin</span><span class="sxs-lookup"><span data-stu-id="55ebb-115">IID_IProfAdmin</span></span>  <br/> |
|<span data-ttu-id="55ebb-116">Tipo de ponteiro:</span><span class="sxs-lookup"><span data-stu-id="55ebb-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="55ebb-117">LPPROFADMIN</span><span class="sxs-lookup"><span data-stu-id="55ebb-117">LPPROFADMIN</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="55ebb-118">Ordem vtable</span><span class="sxs-lookup"><span data-stu-id="55ebb-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="55ebb-119">GetLastError</span><span class="sxs-lookup"><span data-stu-id="55ebb-119">GetLastError</span></span>](iprofadmin-getlasterror.md) <br/> |<span data-ttu-id="55ebb-120">Retorna uma estrutura [MAPIERROR](mapierror.md) que contém informações sobre o erro anterior que ocorreram com um objeto de administração do perfil.</span><span class="sxs-lookup"><span data-stu-id="55ebb-120">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error that occurred to a profile administration object.</span></span>  <br/> |
|[<span data-ttu-id="55ebb-121">GetProfileTable</span><span class="sxs-lookup"><span data-stu-id="55ebb-121">GetProfileTable</span></span>](iprofadmin-getprofiletable.md) <br/> |<span data-ttu-id="55ebb-122">Fornece acesso à tabela de perfis, uma tabela que contém informações sobre todos os perfis disponíveis.</span><span class="sxs-lookup"><span data-stu-id="55ebb-122">Provides access to the profile table, a table that contains information about all of the available profiles.</span></span>  <br/> |
|[<span data-ttu-id="55ebb-123">CreateProfile</span><span class="sxs-lookup"><span data-stu-id="55ebb-123">CreateProfile</span></span>](iprofadmin-createprofile.md) <br/> |<span data-ttu-id="55ebb-124">Cria um novo perfil.</span><span class="sxs-lookup"><span data-stu-id="55ebb-124">Creates a new profile.</span></span>  <br/> |
|[<span data-ttu-id="55ebb-125">DeleteProfile</span><span class="sxs-lookup"><span data-stu-id="55ebb-125">DeleteProfile</span></span>](iprofadmin-deleteprofile.md) <br/> |<span data-ttu-id="55ebb-126">Exclui um perfil.</span><span class="sxs-lookup"><span data-stu-id="55ebb-126">Deletes a profile.</span></span>  <br/> |
|[<span data-ttu-id="55ebb-127">ChangeProfilePassword</span><span class="sxs-lookup"><span data-stu-id="55ebb-127">ChangeProfilePassword</span></span>](iprofadmin-changeprofilepassword.md) <br/> |<span data-ttu-id="55ebb-128">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="55ebb-128">Deprecated.</span></span> <span data-ttu-id="55ebb-129">Altera a senha de um perfil.</span><span class="sxs-lookup"><span data-stu-id="55ebb-129">Changes the password for a profile.</span></span>  <br/> |
|[<span data-ttu-id="55ebb-130">CopyProfile</span><span class="sxs-lookup"><span data-stu-id="55ebb-130">CopyProfile</span></span>](iprofadmin-copyprofile.md) <br/> |<span data-ttu-id="55ebb-131">Copia um perfil.</span><span class="sxs-lookup"><span data-stu-id="55ebb-131">Copies a profile.</span></span>  <br/> |
|[<span data-ttu-id="55ebb-132">RenameProfile</span><span class="sxs-lookup"><span data-stu-id="55ebb-132">RenameProfile</span></span>](iprofadmin-renameprofile.md) <br/> |<span data-ttu-id="55ebb-133">Atribui um novo nome a um perfil.</span><span class="sxs-lookup"><span data-stu-id="55ebb-133">Assigns a new name to a profile.</span></span>  <br/> |
|[<span data-ttu-id="55ebb-134">SetDefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55ebb-134">SetDefaultProfile</span></span>](iprofadmin-setdefaultprofile.md) <br/> |<span data-ttu-id="55ebb-135">Define ou limpa o perfil padrão de um cliente.</span><span class="sxs-lookup"><span data-stu-id="55ebb-135">Sets or clears a client's default profile.</span></span>  <br/> |
|[<span data-ttu-id="55ebb-136">AdminServices</span><span class="sxs-lookup"><span data-stu-id="55ebb-136">AdminServices</span></span>](iprofadmin-adminservices.md) <br/> |<span data-ttu-id="55ebb-137">Fornece acesso a um objeto de administração do serviço de mensagem para aplicar alterações para os serviços de mensagem em um perfil.</span><span class="sxs-lookup"><span data-stu-id="55ebb-137">Provides access to a message service administration object for making changes to the message services in a profile.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="55ebb-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="55ebb-138">See also</span></span>



[<span data-ttu-id="55ebb-139">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="55ebb-139">MAPI Interfaces</span></span>](mapi-interfaces.md)

