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
ms.openlocfilehash: 2e1cff8148815c3e03b92e4d57d1c6a303943c9c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578161"
---
# <a name="pidtagresourcemethods-canonical-property"></a><span data-ttu-id="5fc51-103">Propriedade canônica PidTagResourceMethods</span><span class="sxs-lookup"><span data-stu-id="5fc51-103">PidTagResourceMethods Canonical Property</span></span>

  
  
<span data-ttu-id="5fc51-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5fc51-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5fc51-105">Contém uma bitmask dos sinalizadores que indicam os métodos na interface do **IMAPIStatus** que são compatíveis com o objeto de status.</span><span class="sxs-lookup"><span data-stu-id="5fc51-105">Contains a bitmask of flags that indicate the methods in the **IMAPIStatus** interface that are supported by the status object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5fc51-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="5fc51-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5fc51-107">PR_RESOURCE_METHODS</span><span class="sxs-lookup"><span data-stu-id="5fc51-107">PR_RESOURCE_METHODS</span></span>  <br/> |
|<span data-ttu-id="5fc51-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="5fc51-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5fc51-109">0x3E02</span><span class="sxs-lookup"><span data-stu-id="5fc51-109">0x3E02</span></span>  <br/> |
|<span data-ttu-id="5fc51-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="5fc51-110">Data type:</span></span>  <br/> |<span data-ttu-id="5fc51-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="5fc51-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="5fc51-112">Área:</span><span class="sxs-lookup"><span data-stu-id="5fc51-112">Area:</span></span>  <br/> |<span data-ttu-id="5fc51-113">Status MAPI</span><span class="sxs-lookup"><span data-stu-id="5fc51-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5fc51-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="5fc51-114">Remarks</span></span>

<span data-ttu-id="5fc51-115">Esta propriedade indica que os métodos de implementação de um objeto status de **IMAPIStatus** são suportados.</span><span class="sxs-lookup"><span data-stu-id="5fc51-115">This property indicates which of the methods in a status object's implementation of **IMAPIStatus** are supported.</span></span> <span data-ttu-id="5fc51-116">Objetos de status são permitidos para retornar MAPI_E_NO_SUPPORT de métodos não suportados.</span><span class="sxs-lookup"><span data-stu-id="5fc51-116">Status objects are allowed to return MAPI_E_NO_SUPPORT from unsupported methods.</span></span> 
  
<span data-ttu-id="5fc51-117">Clientes usam status **PR_RESOURCE_METHODS** propriedade de um objeto para evitar fazer chamadas para os métodos sem suporte.</span><span class="sxs-lookup"><span data-stu-id="5fc51-117">Clients use a status object's **PR_RESOURCE_METHODS** property to avoid making calls to unsupported methods.</span></span> <span data-ttu-id="5fc51-118">Se o sinalizador que corresponde a um determinado método for definido, o método existe e pode ser chamado.</span><span class="sxs-lookup"><span data-stu-id="5fc51-118">If the flag that corresponds to a particular method is set, the method exists and can be called.</span></span> <span data-ttu-id="5fc51-119">Se esse sinalizador estiver desmarcada, o método não deve ser chamado.</span><span class="sxs-lookup"><span data-stu-id="5fc51-119">If that flag is clear, the method should not be called.</span></span> 
  
<span data-ttu-id="5fc51-120">Os objetos de status implementadas pelo suporte a MAPI os seguintes métodos:</span><span class="sxs-lookup"><span data-stu-id="5fc51-120">The status objects implemented by MAPI support the following methods:</span></span>
  
|<span data-ttu-id="5fc51-121">**Objeto de status**</span><span class="sxs-lookup"><span data-stu-id="5fc51-121">**Status object**</span></span>|<span data-ttu-id="5fc51-122">**Métodos com suporte**</span><span class="sxs-lookup"><span data-stu-id="5fc51-122">**Supported methods**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5fc51-123">Subsistema MAPI</span><span class="sxs-lookup"><span data-stu-id="5fc51-123">MAPI subsystem</span></span>  <br/> |<span data-ttu-id="5fc51-124">**ValidateState** apenas</span><span class="sxs-lookup"><span data-stu-id="5fc51-124">**ValidateState** only</span></span>  <br/> |
|<span data-ttu-id="5fc51-125">Catálogo de endereços MAPI</span><span class="sxs-lookup"><span data-stu-id="5fc51-125">MAPI address book</span></span>  <br/> |<span data-ttu-id="5fc51-126">**ValidateState** apenas</span><span class="sxs-lookup"><span data-stu-id="5fc51-126">**ValidateState** only</span></span>  <br/> |
|<span data-ttu-id="5fc51-127">Spooler MAPI</span><span class="sxs-lookup"><span data-stu-id="5fc51-127">MAPI spooler</span></span>  <br/> |<span data-ttu-id="5fc51-128">**ValidateState** e **FlushQueues**</span><span class="sxs-lookup"><span data-stu-id="5fc51-128">**ValidateState** and **FlushQueues**</span></span> <br/> |
   
<span data-ttu-id="5fc51-129">Um ou mais dos seguintes sinalizadores podem ser definido em **PR_RESOURCE_METHODS**:</span><span class="sxs-lookup"><span data-stu-id="5fc51-129">One or more of the following flags can be set in **PR_RESOURCE_METHODS**:</span></span>
  
<span data-ttu-id="5fc51-130">STATUS_CHANGE_PASSWORD</span><span class="sxs-lookup"><span data-stu-id="5fc51-130">STATUS_CHANGE_PASSWORD</span></span> 
  
> <span data-ttu-id="5fc51-131">Indica que o método [IMAPIStatus:: ChangePassword](imapistatus-changepassword.md) é suportado.</span><span class="sxs-lookup"><span data-stu-id="5fc51-131">Indicates that the [IMAPIStatus::ChangePassword](imapistatus-changepassword.md) method is supported.</span></span> 
    
<span data-ttu-id="5fc51-132">STATUS_FLUSH_QUEUES</span><span class="sxs-lookup"><span data-stu-id="5fc51-132">STATUS_FLUSH_QUEUES</span></span> 
  
> <span data-ttu-id="5fc51-133">Indica que o método [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) é suportado.</span><span class="sxs-lookup"><span data-stu-id="5fc51-133">Indicates that the [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) method is supported.</span></span> 
    
<span data-ttu-id="5fc51-134">STATUS_SETTINGS_DIALOG</span><span class="sxs-lookup"><span data-stu-id="5fc51-134">STATUS_SETTINGS_DIALOG</span></span> 
  
> <span data-ttu-id="5fc51-135">Indica que o método [IMAPIStatus:: SettingsDialog](imapistatus-settingsdialog.md) é suportado.</span><span class="sxs-lookup"><span data-stu-id="5fc51-135">Indicates that the [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) method is supported.</span></span> 
    
<span data-ttu-id="5fc51-136">STATUS_VALIDATE_STATE</span><span class="sxs-lookup"><span data-stu-id="5fc51-136">STATUS_VALIDATE_STATE</span></span> 
  
> <span data-ttu-id="5fc51-137">Indica que o método [IMAPIStatus::ValidateState](imapistatus-validatestate.md) é suportado.</span><span class="sxs-lookup"><span data-stu-id="5fc51-137">Indicates that the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method is supported.</span></span> 
    
## <a name="related-resources"></a><span data-ttu-id="5fc51-138">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="5fc51-138">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="5fc51-139">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="5fc51-139">Header files</span></span>

<span data-ttu-id="5fc51-140">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5fc51-140">Mapidefs.h</span></span>
  
> <span data-ttu-id="5fc51-141">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="5fc51-141">Provides data type definitions.</span></span>
    
<span data-ttu-id="5fc51-142">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="5fc51-142">Mapitags.h</span></span>
  
> <span data-ttu-id="5fc51-143">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="5fc51-143">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5fc51-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="5fc51-144">See also</span></span>



[<span data-ttu-id="5fc51-145">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="5fc51-145">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5fc51-146">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="5fc51-146">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5fc51-147">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="5fc51-147">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5fc51-148">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="5fc51-148">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

