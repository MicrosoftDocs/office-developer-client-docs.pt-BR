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
ms.openlocfilehash: 28dd45f29610b7ad56b4d3302715311569d497c4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577412"
---
# <a name="iprofadmin--iunknown"></a><span data-ttu-id="e3fc1-103">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e3fc1-103">IProfAdmin : IUnknown</span></span>

  
  
<span data-ttu-id="e3fc1-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e3fc1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e3fc1-105">Oferece suporte a administração de perfis.</span><span class="sxs-lookup"><span data-stu-id="e3fc1-105">Supports the administration of profiles.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e3fc1-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="e3fc1-106">Header file:</span></span>  <br/> |<span data-ttu-id="e3fc1-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="e3fc1-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="e3fc1-108">Expostos pelo:</span><span class="sxs-lookup"><span data-stu-id="e3fc1-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="e3fc1-109">Objeto de administração de perfil</span><span class="sxs-lookup"><span data-stu-id="e3fc1-109">Profile administration object</span></span>  <br/> |
|<span data-ttu-id="e3fc1-110">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="e3fc1-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="e3fc1-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="e3fc1-111">MAPI</span></span>  <br/> |
|<span data-ttu-id="e3fc1-112">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="e3fc1-112">Called by:</span></span>  <br/> |<span data-ttu-id="e3fc1-113">Aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="e3fc1-113">Client applications</span></span>  <br/> |
|<span data-ttu-id="e3fc1-114">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="e3fc1-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="e3fc1-115">IID_IProfAdmin</span><span class="sxs-lookup"><span data-stu-id="e3fc1-115">IID_IProfAdmin</span></span>  <br/> |
|<span data-ttu-id="e3fc1-116">Tipo de ponteiro:</span><span class="sxs-lookup"><span data-stu-id="e3fc1-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="e3fc1-117">LPPROFADMIN</span><span class="sxs-lookup"><span data-stu-id="e3fc1-117">LPPROFADMIN</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="e3fc1-118">Ordem vtable</span><span class="sxs-lookup"><span data-stu-id="e3fc1-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="e3fc1-119">GetLastError</span><span class="sxs-lookup"><span data-stu-id="e3fc1-119">GetLastError</span></span>](iprofadmin-getlasterror.md) <br/> |<span data-ttu-id="e3fc1-120">Retorna uma estrutura [MAPIERROR](mapierror.md) que contém informações sobre o erro anterior que ocorreram com um objeto de administração do perfil.</span><span class="sxs-lookup"><span data-stu-id="e3fc1-120">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error that occurred to a profile administration object.</span></span>  <br/> |
|[<span data-ttu-id="e3fc1-121">GetProfileTable</span><span class="sxs-lookup"><span data-stu-id="e3fc1-121">GetProfileTable</span></span>](iprofadmin-getprofiletable.md) <br/> |<span data-ttu-id="e3fc1-122">Fornece acesso à tabela de perfis, uma tabela que contém informações sobre todos os perfis disponíveis.</span><span class="sxs-lookup"><span data-stu-id="e3fc1-122">Provides access to the profile table, a table that contains information about all of the available profiles.</span></span>  <br/> |
|[<span data-ttu-id="e3fc1-123">CreateProfile</span><span class="sxs-lookup"><span data-stu-id="e3fc1-123">CreateProfile</span></span>](iprofadmin-createprofile.md) <br/> |<span data-ttu-id="e3fc1-124">Cria um novo perfil.</span><span class="sxs-lookup"><span data-stu-id="e3fc1-124">Creates a new profile.</span></span>  <br/> |
|[<span data-ttu-id="e3fc1-125">DeleteProfile</span><span class="sxs-lookup"><span data-stu-id="e3fc1-125">DeleteProfile</span></span>](iprofadmin-deleteprofile.md) <br/> |<span data-ttu-id="e3fc1-126">Exclui um perfil.</span><span class="sxs-lookup"><span data-stu-id="e3fc1-126">Deletes a profile.</span></span>  <br/> |
|[<span data-ttu-id="e3fc1-127">ChangeProfilePassword</span><span class="sxs-lookup"><span data-stu-id="e3fc1-127">ChangeProfilePassword</span></span>](iprofadmin-changeprofilepassword.md) <br/> |<span data-ttu-id="e3fc1-128">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="e3fc1-128">Deprecated.</span></span> <span data-ttu-id="e3fc1-129">Altera a senha de um perfil.</span><span class="sxs-lookup"><span data-stu-id="e3fc1-129">Changes the password for a profile.</span></span>  <br/> |
|[<span data-ttu-id="e3fc1-130">CopyProfile</span><span class="sxs-lookup"><span data-stu-id="e3fc1-130">CopyProfile</span></span>](iprofadmin-copyprofile.md) <br/> |<span data-ttu-id="e3fc1-131">Copia um perfil.</span><span class="sxs-lookup"><span data-stu-id="e3fc1-131">Copies a profile.</span></span>  <br/> |
|[<span data-ttu-id="e3fc1-132">RenameProfile</span><span class="sxs-lookup"><span data-stu-id="e3fc1-132">RenameProfile</span></span>](iprofadmin-renameprofile.md) <br/> |<span data-ttu-id="e3fc1-133">Atribui um novo nome a um perfil.</span><span class="sxs-lookup"><span data-stu-id="e3fc1-133">Assigns a new name to a profile.</span></span>  <br/> |
|[<span data-ttu-id="e3fc1-134">SetDefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3fc1-134">SetDefaultProfile</span></span>](iprofadmin-setdefaultprofile.md) <br/> |<span data-ttu-id="e3fc1-135">Define ou limpa o perfil padrão de um cliente.</span><span class="sxs-lookup"><span data-stu-id="e3fc1-135">Sets or clears a client's default profile.</span></span>  <br/> |
|[<span data-ttu-id="e3fc1-136">AdminServices</span><span class="sxs-lookup"><span data-stu-id="e3fc1-136">AdminServices</span></span>](iprofadmin-adminservices.md) <br/> |<span data-ttu-id="e3fc1-137">Fornece acesso a um objeto de administração do serviço de mensagem para aplicar alterações para os serviços de mensagem em um perfil.</span><span class="sxs-lookup"><span data-stu-id="e3fc1-137">Provides access to a message service administration object for making changes to the message services in a profile.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e3fc1-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="e3fc1-138">See also</span></span>



[<span data-ttu-id="e3fc1-139">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="e3fc1-139">MAPI Interfaces</span></span>](mapi-interfaces.md)

