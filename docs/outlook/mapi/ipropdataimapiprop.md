---
title: IPropData IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPropData
api_type:
- COM
ms.assetid: 30b8ae9e-0c0c-4468-b286-29e083696fed
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: aed9120ac264a6c47c9d02502093e56d3268d08a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435142"
---
# <a name="ipropdata--imapiprop"></a><span data-ttu-id="483c3-103">IPropData : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="483c3-103">IPropData : IMAPIProp</span></span>

  
  
<span data-ttu-id="483c3-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="483c3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="483c3-105">Fornece a capacidade de recuperar e alterar o acesso para as propriedades de um objeto.</span><span class="sxs-lookup"><span data-stu-id="483c3-105">Provides the ability to retrieve and change the access for an object's properties.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="483c3-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="483c3-106">Header file:</span></span>  <br/> |<span data-ttu-id="483c3-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="483c3-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="483c3-108">Exposto por:</span><span class="sxs-lookup"><span data-stu-id="483c3-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="483c3-109">Objeto de dados de propriedade</span><span class="sxs-lookup"><span data-stu-id="483c3-109">Property data object</span></span>  <br/> |
|<span data-ttu-id="483c3-110">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="483c3-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="483c3-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="483c3-111">MAPI</span></span>  <br/> |
|<span data-ttu-id="483c3-112">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="483c3-112">Called by:</span></span>  <br/> |<span data-ttu-id="483c3-113">Provedores de serviços e aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="483c3-113">Service providers and client applications</span></span>  <br/> |
|<span data-ttu-id="483c3-114">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="483c3-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="483c3-115">IID_IMAPIPropData</span><span class="sxs-lookup"><span data-stu-id="483c3-115">IID_IMAPIPropData</span></span>  <br/> |
|<span data-ttu-id="483c3-116">Tipo de ponteiro:</span><span class="sxs-lookup"><span data-stu-id="483c3-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="483c3-117">LPPROPDATA</span><span class="sxs-lookup"><span data-stu-id="483c3-117">LPPROPDATA</span></span>  <br/> |
|<span data-ttu-id="483c3-118">Modelo de transação:</span><span class="sxs-lookup"><span data-stu-id="483c3-118">Transaction model:</span></span>  <br/> |<span data-ttu-id="483c3-119">Não-Transacted</span><span class="sxs-lookup"><span data-stu-id="483c3-119">Nontransacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="483c3-120">Vtable order</span><span class="sxs-lookup"><span data-stu-id="483c3-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="483c3-121">HrSetObjAccess</span><span class="sxs-lookup"><span data-stu-id="483c3-121">HrSetObjAccess</span></span>](ipropdata-hrsetobjaccess.md) <br/> |<span data-ttu-id="483c3-122">Define o n�vel de acesso para o objeto.</span><span class="sxs-lookup"><span data-stu-id="483c3-122">Sets the access level for the object.</span></span>  <br/> |
|[<span data-ttu-id="483c3-123">HrSetPropAccess</span><span class="sxs-lookup"><span data-stu-id="483c3-123">HrSetPropAccess</span></span>](ipropdata-hrsetpropaccess.md) <br/> |<span data-ttu-id="483c3-124">Define o nível de acesso e o status de uma ou mais propriedades do objeto.</span><span class="sxs-lookup"><span data-stu-id="483c3-124">Sets the access level and status for one or more of the object's properties.</span></span>  <br/> |
|[<span data-ttu-id="483c3-125">HrGetPropAccess</span><span class="sxs-lookup"><span data-stu-id="483c3-125">HrGetPropAccess</span></span>](ipropdata-hrgetpropaccess.md) <br/> |<span data-ttu-id="483c3-126">Recupera o n�vel de acesso e o status de uma ou mais das propriedades do objeto.</span><span class="sxs-lookup"><span data-stu-id="483c3-126">Retrieves the access level and status for one or more of the object's properties.</span></span>  <br/> |
|[<span data-ttu-id="483c3-127">HrAddObjProps</span><span class="sxs-lookup"><span data-stu-id="483c3-127">HrAddObjProps</span></span>](ipropdata-hraddobjprops.md) <br/> |<span data-ttu-id="483c3-128">Adiciona uma ou mais propriedades do tipo PT_OBJECT ao objeto.</span><span class="sxs-lookup"><span data-stu-id="483c3-128">Adds one or more properties of type PT_OBJECT to the object.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="483c3-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="483c3-129">Remarks</span></span>

<span data-ttu-id="483c3-130">A interface **IPropData:: IMAPIProp** é implementada pelo MAPI e é usada principalmente por provedores de serviços que acessam essa implementação chamando a função [CreateIProp](createiprop.md) .</span><span class="sxs-lookup"><span data-stu-id="483c3-130">The **IPropData::IMAPIProp** interface is implemented by MAPI and used primarily by service providers that access this implementation by calling the [CreateIProp](createiprop.md) function.</span></span> 
  
<span data-ttu-id="483c3-131">Para obter mais informações sobre níveis de acesso em objetos e propriedades, consulte [permissões para objetos e propriedades](permissions-for-mapi-objects-and-properties.md).</span><span class="sxs-lookup"><span data-stu-id="483c3-131">For more information about access levels on objects and properties, see [Permissions for Objects and Properties](permissions-for-mapi-objects-and-properties.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="483c3-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="483c3-132">See also</span></span>



[<span data-ttu-id="483c3-133">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="483c3-133">MAPI Interfaces</span></span>](mapi-interfaces.md)

