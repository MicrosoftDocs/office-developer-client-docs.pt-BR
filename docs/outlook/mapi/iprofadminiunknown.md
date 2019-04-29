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
ms.openlocfilehash: cbdfba68490b1e756f277c6e552235368a86f310
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434113"
---
# <a name="iprofadmin--iunknown"></a><span data-ttu-id="3899b-103">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3899b-103">IProfAdmin : IUnknown</span></span>

  
  
<span data-ttu-id="3899b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3899b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3899b-105">Oferece suporte à administração de perfis.</span><span class="sxs-lookup"><span data-stu-id="3899b-105">Supports the administration of profiles.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3899b-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="3899b-106">Header file:</span></span>  <br/> |<span data-ttu-id="3899b-107">Mapix. h</span><span class="sxs-lookup"><span data-stu-id="3899b-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="3899b-108">Exposto por:</span><span class="sxs-lookup"><span data-stu-id="3899b-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="3899b-109">Objeto de administração de perfil</span><span class="sxs-lookup"><span data-stu-id="3899b-109">Profile administration object</span></span>  <br/> |
|<span data-ttu-id="3899b-110">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="3899b-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="3899b-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="3899b-111">MAPI</span></span>  <br/> |
|<span data-ttu-id="3899b-112">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="3899b-112">Called by:</span></span>  <br/> |<span data-ttu-id="3899b-113">Aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="3899b-113">Client applications</span></span>  <br/> |
|<span data-ttu-id="3899b-114">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="3899b-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="3899b-115">IID_IProfAdmin</span><span class="sxs-lookup"><span data-stu-id="3899b-115">IID_IProfAdmin</span></span>  <br/> |
|<span data-ttu-id="3899b-116">Tipo de ponteiro:</span><span class="sxs-lookup"><span data-stu-id="3899b-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="3899b-117">LPPROFADMIN</span><span class="sxs-lookup"><span data-stu-id="3899b-117">LPPROFADMIN</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="3899b-118">Vtable order</span><span class="sxs-lookup"><span data-stu-id="3899b-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="3899b-119">GetLastError</span><span class="sxs-lookup"><span data-stu-id="3899b-119">GetLastError</span></span>](iprofadmin-getlasterror.md) <br/> |<span data-ttu-id="3899b-120">Retorna uma estrutura [MAPIERROR](mapierror.md) que contém informações sobre o erro anterior que ocorreu com um objeto de administração de perfil.</span><span class="sxs-lookup"><span data-stu-id="3899b-120">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error that occurred to a profile administration object.</span></span>  <br/> |
|[<span data-ttu-id="3899b-121">GetProfiletable</span><span class="sxs-lookup"><span data-stu-id="3899b-121">GetProfileTable</span></span>](iprofadmin-getprofiletable.md) <br/> |<span data-ttu-id="3899b-122">Fornece acesso à tabela de perfil, uma tabela que contém informações sobre todos os perfis disponíveis.</span><span class="sxs-lookup"><span data-stu-id="3899b-122">Provides access to the profile table, a table that contains information about all of the available profiles.</span></span>  <br/> |
|[<span data-ttu-id="3899b-123">CreateProfile</span><span class="sxs-lookup"><span data-stu-id="3899b-123">CreateProfile</span></span>](iprofadmin-createprofile.md) <br/> |<span data-ttu-id="3899b-124">Cria um novo perfil.</span><span class="sxs-lookup"><span data-stu-id="3899b-124">Creates a new profile.</span></span>  <br/> |
|[<span data-ttu-id="3899b-125">DeleteProfile</span><span class="sxs-lookup"><span data-stu-id="3899b-125">DeleteProfile</span></span>](iprofadmin-deleteprofile.md) <br/> |<span data-ttu-id="3899b-126">Exclui um perfil.</span><span class="sxs-lookup"><span data-stu-id="3899b-126">Deletes a profile.</span></span>  <br/> |
|[<span data-ttu-id="3899b-127">ChangeProfilePassword</span><span class="sxs-lookup"><span data-stu-id="3899b-127">ChangeProfilePassword</span></span>](iprofadmin-changeprofilepassword.md) <br/> |<span data-ttu-id="3899b-128">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="3899b-128">Deprecated.</span></span> <span data-ttu-id="3899b-129">Altera a senha de um perfil.</span><span class="sxs-lookup"><span data-stu-id="3899b-129">Changes the password for a profile.</span></span>  <br/> |
|[<span data-ttu-id="3899b-130">CopyProfile</span><span class="sxs-lookup"><span data-stu-id="3899b-130">CopyProfile</span></span>](iprofadmin-copyprofile.md) <br/> |<span data-ttu-id="3899b-131">Copia um perfil.</span><span class="sxs-lookup"><span data-stu-id="3899b-131">Copies a profile.</span></span>  <br/> |
|[<span data-ttu-id="3899b-132">RenameProfile</span><span class="sxs-lookup"><span data-stu-id="3899b-132">RenameProfile</span></span>](iprofadmin-renameprofile.md) <br/> |<span data-ttu-id="3899b-133">Atribui um novo nome a um perfil.</span><span class="sxs-lookup"><span data-stu-id="3899b-133">Assigns a new name to a profile.</span></span>  <br/> |
|[<span data-ttu-id="3899b-134">Setdefaultprofile foi</span><span class="sxs-lookup"><span data-stu-id="3899b-134">SetDefaultProfile</span></span>](iprofadmin-setdefaultprofile.md) <br/> |<span data-ttu-id="3899b-135">Define ou limpa o perfil padrão de um cliente.</span><span class="sxs-lookup"><span data-stu-id="3899b-135">Sets or clears a client's default profile.</span></span>  <br/> |
|[<span data-ttu-id="3899b-136">Adminservices</span><span class="sxs-lookup"><span data-stu-id="3899b-136">AdminServices</span></span>](iprofadmin-adminservices.md) <br/> |<span data-ttu-id="3899b-137">Fornece acesso a um objeto de administração de serviço de mensagens para fazer alterações nos serviços de mensagens em um perfil.</span><span class="sxs-lookup"><span data-stu-id="3899b-137">Provides access to a message service administration object for making changes to the message services in a profile.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3899b-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="3899b-138">See also</span></span>



[<span data-ttu-id="3899b-139">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="3899b-139">MAPI Interfaces</span></span>](mapi-interfaces.md)

