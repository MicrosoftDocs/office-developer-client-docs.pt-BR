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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: d6a53d112e4c12cd9092ac627e99cf3c13d901f3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767639"
---
# <a name="ipropdata--imapiprop"></a><span data-ttu-id="ddb1d-103">IPropData: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="ddb1d-103">IPropData : IMAPIProp</span></span>

  
  
<span data-ttu-id="ddb1d-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ddb1d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ddb1d-105">Fornece a capacidade de recuperar e alterar o acesso para propriedades de um objeto.</span><span class="sxs-lookup"><span data-stu-id="ddb1d-105">Provides the ability to retrieve and change the access for an object's properties.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ddb1d-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="ddb1d-106">Header file:</span></span>  <br/> |<span data-ttu-id="ddb1d-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="ddb1d-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="ddb1d-108">Expostos pelo:</span><span class="sxs-lookup"><span data-stu-id="ddb1d-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="ddb1d-109">Objeto de dados de propriedade</span><span class="sxs-lookup"><span data-stu-id="ddb1d-109">Property data object</span></span>  <br/> |
|<span data-ttu-id="ddb1d-110">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="ddb1d-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="ddb1d-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="ddb1d-111">MAPI</span></span>  <br/> |
|<span data-ttu-id="ddb1d-112">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="ddb1d-112">Called by:</span></span>  <br/> |<span data-ttu-id="ddb1d-113">Provedores de serviços e aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="ddb1d-113">Service providers and client applications</span></span>  <br/> |
|<span data-ttu-id="ddb1d-114">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="ddb1d-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="ddb1d-115">IID_IMAPIPropData</span><span class="sxs-lookup"><span data-stu-id="ddb1d-115">IID_IMAPIPropData</span></span>  <br/> |
|<span data-ttu-id="ddb1d-116">Tipo de ponteiro:</span><span class="sxs-lookup"><span data-stu-id="ddb1d-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="ddb1d-117">LPPROPDATA</span><span class="sxs-lookup"><span data-stu-id="ddb1d-117">LPPROPDATA</span></span>  <br/> |
|<span data-ttu-id="ddb1d-118">Modelo de transação:</span><span class="sxs-lookup"><span data-stu-id="ddb1d-118">Transaction model:</span></span>  <br/> |<span data-ttu-id="ddb1d-119">Nontransacted</span><span class="sxs-lookup"><span data-stu-id="ddb1d-119">Nontransacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="ddb1d-120">Ordem vtable</span><span class="sxs-lookup"><span data-stu-id="ddb1d-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="ddb1d-121">HrSetObjAccess</span><span class="sxs-lookup"><span data-stu-id="ddb1d-121">HrSetObjAccess</span></span>](ipropdata-hrsetobjaccess.md) <br/> |<span data-ttu-id="ddb1d-122">Define o n�vel de acesso para o objeto.</span><span class="sxs-lookup"><span data-stu-id="ddb1d-122">Sets the access level for the object.</span></span>  <br/> |
|[<span data-ttu-id="ddb1d-123">HrSetPropAccess</span><span class="sxs-lookup"><span data-stu-id="ddb1d-123">HrSetPropAccess</span></span>](ipropdata-hrsetpropaccess.md) <br/> |<span data-ttu-id="ddb1d-124">Define o nível de acesso e o status de uma ou mais das propriedades do objeto.</span><span class="sxs-lookup"><span data-stu-id="ddb1d-124">Sets the access level and status for one or more of the object's properties.</span></span>  <br/> |
|[<span data-ttu-id="ddb1d-125">HrGetPropAccess</span><span class="sxs-lookup"><span data-stu-id="ddb1d-125">HrGetPropAccess</span></span>](ipropdata-hrgetpropaccess.md) <br/> |<span data-ttu-id="ddb1d-126">Recupera o n�vel de acesso e o status de uma ou mais das propriedades do objeto.</span><span class="sxs-lookup"><span data-stu-id="ddb1d-126">Retrieves the access level and status for one or more of the object's properties.</span></span>  <br/> |
|[<span data-ttu-id="ddb1d-127">HrAddObjProps</span><span class="sxs-lookup"><span data-stu-id="ddb1d-127">HrAddObjProps</span></span>](ipropdata-hraddobjprops.md) <br/> |<span data-ttu-id="ddb1d-128">Adiciona uma ou mais propriedades do tipo PT_OBJECT ao objeto.</span><span class="sxs-lookup"><span data-stu-id="ddb1d-128">Adds one or more properties of type PT_OBJECT to the object.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ddb1d-129">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="ddb1d-129">Remarks</span></span>

<span data-ttu-id="ddb1d-130">A interface **IPropData::IMAPIProp** é implementada por MAPI e usada principalmente pelos provedores de serviços que acessam essa implementação chamando a função [CreateIProp](createiprop.md) .</span><span class="sxs-lookup"><span data-stu-id="ddb1d-130">The **IPropData::IMAPIProp** interface is implemented by MAPI and used primarily by service providers that access this implementation by calling the [CreateIProp](createiprop.md) function.</span></span> 
  
<span data-ttu-id="ddb1d-131">Para obter mais informações sobre níveis de acesso em objetos e propriedades, consulte [permissões para objetos e propriedades](permissions-for-mapi-objects-and-properties.md).</span><span class="sxs-lookup"><span data-stu-id="ddb1d-131">For more information about access levels on objects and properties, see [Permissions for Objects and Properties](permissions-for-mapi-objects-and-properties.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ddb1d-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="ddb1d-132">See also</span></span>



[<span data-ttu-id="ddb1d-133">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="ddb1d-133">MAPI Interfaces</span></span>](mapi-interfaces.md)

