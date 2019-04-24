---
title: Propriedade canônica PidTagResourceMethods
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagResourceMethods
api_type:
- COM
ms.assetid: 60ebbcd5-b758-4c96-b8ec-089e0aae1a5f
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: e9aee3280edbed60e97ef6e00e61f3086f6f07ce
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330139"
---
# <a name="pidtagresourcemethods-canonical-property"></a><span data-ttu-id="afdec-103">Propriedade canônica PidTagResourceMethods</span><span class="sxs-lookup"><span data-stu-id="afdec-103">PidTagResourceMethods Canonical Property</span></span>

  
  
<span data-ttu-id="afdec-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="afdec-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="afdec-105">Contém uma bitmask de sinalizadores que indicam os métodos na interface **IMAPIStatus** que são compatíveis com o objeto status.</span><span class="sxs-lookup"><span data-stu-id="afdec-105">Contains a bitmask of flags that indicate the methods in the **IMAPIStatus** interface that are supported by the status object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="afdec-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="afdec-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="afdec-107">PR_RESOURCE_METHODS</span><span class="sxs-lookup"><span data-stu-id="afdec-107">PR_RESOURCE_METHODS</span></span>  <br/> |
|<span data-ttu-id="afdec-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="afdec-108">Identifier:</span></span>  <br/> |<span data-ttu-id="afdec-109">0x3E02</span><span class="sxs-lookup"><span data-stu-id="afdec-109">0x3E02</span></span>  <br/> |
|<span data-ttu-id="afdec-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="afdec-110">Data type:</span></span>  <br/> |<span data-ttu-id="afdec-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="afdec-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="afdec-112">Área:</span><span class="sxs-lookup"><span data-stu-id="afdec-112">Area:</span></span>  <br/> |<span data-ttu-id="afdec-113">Status de MAPI</span><span class="sxs-lookup"><span data-stu-id="afdec-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="afdec-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="afdec-114">Remarks</span></span>

<span data-ttu-id="afdec-115">Essa propriedade indica qual dos métodos na implementação de **IMAPIStatus** de um objeto status são suportados.</span><span class="sxs-lookup"><span data-stu-id="afdec-115">This property indicates which of the methods in a status object's implementation of **IMAPIStatus** are supported.</span></span> <span data-ttu-id="afdec-116">Os objetos de status têm permissão para retornar MAPI_E_NO_SUPPORT de métodos sem suporte.</span><span class="sxs-lookup"><span data-stu-id="afdec-116">Status objects are allowed to return MAPI_E_NO_SUPPORT from unsupported methods.</span></span> 
  
<span data-ttu-id="afdec-117">Os clientes usam a propriedade **PR_RESOURCE_METHODS** de um objeto status para evitar fazer chamadas para métodos sem suporte.</span><span class="sxs-lookup"><span data-stu-id="afdec-117">Clients use a status object's **PR_RESOURCE_METHODS** property to avoid making calls to unsupported methods.</span></span> <span data-ttu-id="afdec-118">Se o sinalizador que corresponde a um determinado método for definido, o método existirá e poderá ser chamado.</span><span class="sxs-lookup"><span data-stu-id="afdec-118">If the flag that corresponds to a particular method is set, the method exists and can be called.</span></span> <span data-ttu-id="afdec-119">Se esse sinalizador for claro, o método não deverá ser chamado.</span><span class="sxs-lookup"><span data-stu-id="afdec-119">If that flag is clear, the method should not be called.</span></span> 
  
<span data-ttu-id="afdec-120">Os objetos de status implementados pelo MAPI dão suporte aos seguintes métodos:</span><span class="sxs-lookup"><span data-stu-id="afdec-120">The status objects implemented by MAPI support the following methods:</span></span>
  
|<span data-ttu-id="afdec-121">**Objeto status**</span><span class="sxs-lookup"><span data-stu-id="afdec-121">**Status object**</span></span>|<span data-ttu-id="afdec-122">**Métodos com suporte**</span><span class="sxs-lookup"><span data-stu-id="afdec-122">**Supported methods**</span></span>|
|:-----|:-----|
|<span data-ttu-id="afdec-123">Subsistema MAPI</span><span class="sxs-lookup"><span data-stu-id="afdec-123">MAPI subsystem</span></span>  <br/> |<span data-ttu-id="afdec-124">**ValidateState** somente</span><span class="sxs-lookup"><span data-stu-id="afdec-124">**ValidateState** only</span></span>  <br/> |
|<span data-ttu-id="afdec-125">Catálogo de endereços MAPI</span><span class="sxs-lookup"><span data-stu-id="afdec-125">MAPI address book</span></span>  <br/> |<span data-ttu-id="afdec-126">**ValidateState** somente</span><span class="sxs-lookup"><span data-stu-id="afdec-126">**ValidateState** only</span></span>  <br/> |
|<span data-ttu-id="afdec-127">Spooler MAPI</span><span class="sxs-lookup"><span data-stu-id="afdec-127">MAPI spooler</span></span>  <br/> |<span data-ttu-id="afdec-128">**ValidateState** e **FlushQueues**</span><span class="sxs-lookup"><span data-stu-id="afdec-128">**ValidateState** and **FlushQueues**</span></span> <br/> |
   
<span data-ttu-id="afdec-129">Um ou mais dos seguintes sinalizadores podem ser definidos no **PR_RESOURCE_METHODS**:</span><span class="sxs-lookup"><span data-stu-id="afdec-129">One or more of the following flags can be set in **PR_RESOURCE_METHODS**:</span></span>
  
<span data-ttu-id="afdec-130">STATUS_CHANGE_PASSWORD</span><span class="sxs-lookup"><span data-stu-id="afdec-130">STATUS_CHANGE_PASSWORD</span></span> 
  
> <span data-ttu-id="afdec-131">Indica que o método [IMAPIStatus:: ChangePassword](imapistatus-changepassword.md) é suportado.</span><span class="sxs-lookup"><span data-stu-id="afdec-131">Indicates that the [IMAPIStatus::ChangePassword](imapistatus-changepassword.md) method is supported.</span></span> 
    
<span data-ttu-id="afdec-132">STATUS_FLUSH_QUEUES</span><span class="sxs-lookup"><span data-stu-id="afdec-132">STATUS_FLUSH_QUEUES</span></span> 
  
> <span data-ttu-id="afdec-133">Indica que há suporte para o método [IMAPIStatus:: FlushQueues](imapistatus-flushqueues.md) .</span><span class="sxs-lookup"><span data-stu-id="afdec-133">Indicates that the [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) method is supported.</span></span> 
    
<span data-ttu-id="afdec-134">STATUS_SETTINGS_DIALOG</span><span class="sxs-lookup"><span data-stu-id="afdec-134">STATUS_SETTINGS_DIALOG</span></span> 
  
> <span data-ttu-id="afdec-135">Indica que há suporte para o método [IMAPIStatus:: SettingsDialog](imapistatus-settingsdialog.md) .</span><span class="sxs-lookup"><span data-stu-id="afdec-135">Indicates that the [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) method is supported.</span></span> 
    
<span data-ttu-id="afdec-136">STATUS_VALIDATE_STATE</span><span class="sxs-lookup"><span data-stu-id="afdec-136">STATUS_VALIDATE_STATE</span></span> 
  
> <span data-ttu-id="afdec-137">Indica que o método [IMAPIStatus:: ValidateState](imapistatus-validatestate.md) é suportado.</span><span class="sxs-lookup"><span data-stu-id="afdec-137">Indicates that the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method is supported.</span></span> 
    
## <a name="related-resources"></a><span data-ttu-id="afdec-138">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="afdec-138">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="afdec-139">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="afdec-139">Header files</span></span>

<span data-ttu-id="afdec-140">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="afdec-140">Mapidefs.h</span></span>
  
> <span data-ttu-id="afdec-141">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="afdec-141">Provides data type definitions.</span></span>
    
<span data-ttu-id="afdec-142">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="afdec-142">Mapitags.h</span></span>
  
> <span data-ttu-id="afdec-143">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="afdec-143">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="afdec-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="afdec-144">See also</span></span>



[<span data-ttu-id="afdec-145">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="afdec-145">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="afdec-146">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="afdec-146">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="afdec-147">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="afdec-147">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="afdec-148">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="afdec-148">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

