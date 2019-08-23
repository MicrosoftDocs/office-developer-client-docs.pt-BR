---
title: Sobre as propriedades nomeadas usadas pelo Outlook
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 8c245ec2-bb18-ecf0-b4ad-8c164c5924cf
description: 'Última modificação: 25 de julho de 2012'
ms.openlocfilehash: 328ff423025689795669d661f529270886123a7e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322236"
---
# <a name="about-named-properties-used-by-outlook"></a><span data-ttu-id="65d66-103">Sobre as propriedades nomeadas usadas pelo Outlook</span><span class="sxs-lookup"><span data-stu-id="65d66-103">About Named Properties Used by Outlook</span></span>

  
  
<span data-ttu-id="65d66-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="65d66-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="65d66-p101">O MAPI fornece um recurso para atribuir nomes a certas propriedades, para mapear esses nomes para identificadores exclusivos e para fazer esse mapeamento nome-para-identificador persistente nas sessões. As propriedades nomeadas são identificadas por um nome e um identificador global exclusivo (GUID) para um conjunto de propriedades. O nome pode ser um número ou uma cadeia de caracteres. No Microsoft Outlook 2013 ou no Microsoft Outlook 2010, o conjunto de propriedades geralmente é um namespace definido pelo Outlook 2013 ou 2010, como **PSETID_Appointment**.</span><span class="sxs-lookup"><span data-stu-id="65d66-p101">MAPI provides a facility for assigning names to certain properties, for mapping these names to unique identifiers, and for making this name-to-identifier mapping persistent across sessions. Named properties are identified by a name and a globally unique identifier (GUID) for a property set. The name can be a number or a string. For Microsoft Outlook 2013 or Microsoft Outlook 2010, the property set is often a namespace defined by Outlook 2013 or Outlook 2010, such as **PSETID_Appointment**.</span></span> 
  
<span data-ttu-id="65d66-p102">Propriedades nomeadas são manipuladas usando a função [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) e a função [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md). O nome e o GUID do conjunto de propriedades são passados para a função [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) para obter um identificador de propriedade que seja válido para a sessão MAPI atual. Como esse identificador de propriedade pode variar entre computadores, a única maneira consistente de acessar uma propriedade nomeada é saber seu nome e GUID do conjunto de propriedades. O intervalo de identificadores está sempre entre 0x8000 e 0xFFFE.</span><span class="sxs-lookup"><span data-stu-id="65d66-p102">Named properties are manipulated by using the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) function and the [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) function. The name and the property set GUID are passed to the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) function to obtain a property identifier that is valid for the current MAPI session. Because this property identifier can vary from computer to computer, the only consistent way to access a named property is to know its name and property set GUID. The range for identifiers is always in the 0x8000 and 0xFFFE range.</span></span> 
  
<span data-ttu-id="65d66-p103">Qualquer objeto que implementa a interface [IMAPIProp: IUnknown](imapipropiunknown.md) pode suportar propriedades nomeadas. Especificamente, um provedor de serviços MAPI ou um cliente MAPI precisa implementar [IMAPIProp::GetProps](imapiprop-getprops.md) para obter valores de propriedades nomeadas. A configuração de propriedades usada pelo Outlook 2013 ou Outlook 2010 não é suportada por causa do risco de corrompimento de dados que é compartilhado com outros provedores ou clientes MAPI.</span><span class="sxs-lookup"><span data-stu-id="65d66-p103">Any object that implements the [IMAPIProp : IUnknown](imapipropiunknown.md) interface can support named properties. Specifically, a MAPI service provider or a MAPI client must implement [IMAPIProp::GetProps](imapiprop-getprops.md) to get values of named properties. Setting named properties used by Outlook 2013 or Outlook 2010 is not supported because of the risk of corrupting data that is shared with other MAPI providers or clients.</span></span> 
  
<span data-ttu-id="65d66-p104">O Outlook 2013 e o Outlook 2010 usam propriedades nomeadas MAPI para implementar muitos de seus recursos; por exemplo, segurança de anexos e contrapropostas de reuniões. Acima desses dados subjacentes, o Outlook 2013 e o Outlook 2010 expõem algumas dessas propriedades como propriedades de itens em seus modelos de objeto do Outlook 2013 e do Outlook 2010. Por exemplo, a propriedade **Email1Address** do objeto **ContactItem** no modelo de objeto corresponde à nomeada [PidLidEmail1EmailAddress](pidlidemail1emailaddress-canonical-property.md) no namespace **PSETID_Address**. Em geral, porém, em razão de preocupações com compatibilidade e integridade de dados, muitas das propriedades MAPI usadas pelo Outlook 2013 e Outlook 2010 não são expostas no modelo de objeto.</span><span class="sxs-lookup"><span data-stu-id="65d66-p104">Outlook 2013 and Outlook 2010 use MAPI named properties to implement many of their features, for example, attachment security and meeting counter-proposals. Above this underlying data, Outlook 2013 and Outlook 2010 expose some of these properties as item properties in their Outlook 2013 and Outlook 2010 object models. For example, the **Email1Address** property of the **ContactItem** object in the object model corresponds to the named [PidLidEmail1EmailAddress Canonical Property](pidlidemail1emailaddress-canonical-property.md) in the **PSETID_Address** namespace. But in general, due to concerns for compatibility and data integrity, many of the MAPI properties that are used by Outlook 2013 and Outlook 2010 are not exposed in the object model.</span></span> 
  
<span data-ttu-id="65d66-120">Esta referência descreve diversas propriedades nomeadas que estão listadas abaixo.</span><span class="sxs-lookup"><span data-stu-id="65d66-120">This reference describes a number of named properties that are listed below.</span></span>
  
<span data-ttu-id="65d66-121">As propriedades nomeadas no namespace **PSETID_Address** são as seguintes:</span><span class="sxs-lookup"><span data-stu-id="65d66-121">Named properties in the **PSETID_Address** namespace are the following:</span></span> 
  
- [<span data-ttu-id="65d66-122">Propriedade canônica PidLidEmail1AddressType</span><span class="sxs-lookup"><span data-stu-id="65d66-122">PidLidEmail1AddressType Canonical Property</span></span>](pidlidemail1addresstype-canonical-property.md)
    
- [<span data-ttu-id="65d66-123">Propriedade canônica PidLidEmail1EmailAddress</span><span class="sxs-lookup"><span data-stu-id="65d66-123">PidLidEmail1EmailAddress Canonical Property</span></span>](pidlidemail1emailaddress-canonical-property.md)
    
- [<span data-ttu-id="65d66-124">Propriedade canônica PidLidEmail1OriginalEntryId</span><span class="sxs-lookup"><span data-stu-id="65d66-124">PidLidEmail1OriginalEntryId Canonical Property</span></span>](pidlidemail1originalentryid-canonical-property.md)
    
- [<span data-ttu-id="65d66-125">Propriedade canônica PidLidEmail2AddressType</span><span class="sxs-lookup"><span data-stu-id="65d66-125">PidLidEmail2AddressType Canonical Property</span></span>](pidlidemail2addresstype-canonical-property.md)
    
- [<span data-ttu-id="65d66-126">Propriedade canônica PidLidEmail2DisplayName</span><span class="sxs-lookup"><span data-stu-id="65d66-126">PidLidEmail2DisplayName Canonical Property</span></span>](pidlidemail2displayname-canonical-property.md)
    
- [<span data-ttu-id="65d66-127">Propriedade canônica PidLidEmail2EmailAddress</span><span class="sxs-lookup"><span data-stu-id="65d66-127">PidLidEmail2EmailAddress Canonical Property</span></span>](pidlidemail2emailaddress-canonical-property.md)
    
- [<span data-ttu-id="65d66-128">Propriedade canônica PidLidEmail2OriginalDisplayName</span><span class="sxs-lookup"><span data-stu-id="65d66-128">PidLidEmail2OriginalDisplayName Canonical Property</span></span>](pidlidemail2originaldisplayname-canonical-property.md)
    
- [<span data-ttu-id="65d66-129">Propriedade canônica PidLidEmail2OriginalEntryId</span><span class="sxs-lookup"><span data-stu-id="65d66-129">PidLidEmail2OriginalEntryId Canonical Property</span></span>](pidlidemail2originalentryid-canonical-property.md)
    
- [<span data-ttu-id="65d66-130">Propriedade canônica PidLidEmail3AddressType</span><span class="sxs-lookup"><span data-stu-id="65d66-130">PidLidEmail3AddressType Canonical Property</span></span>](pidlidemail3addresstype-canonical-property.md)
    
- [<span data-ttu-id="65d66-131">Propriedade canônica PidLidEmail3DisplayName</span><span class="sxs-lookup"><span data-stu-id="65d66-131">PidLidEmail3DisplayName Canonical Property</span></span>](pidlidemail3displayname-canonical-property.md)
    
- [<span data-ttu-id="65d66-132">Propriedade canônica PidLidEmail3EmailAddress</span><span class="sxs-lookup"><span data-stu-id="65d66-132">PidLidEmail3EmailAddress Canonical Property</span></span>](pidlidemail3emailaddress-canonical-property.md)
    
- [<span data-ttu-id="65d66-133">Propriedade canônica PidLidEmail3OriginalDisplayName</span><span class="sxs-lookup"><span data-stu-id="65d66-133">PidLidEmail3OriginalDisplayName Canonical Property</span></span>](pidlidemail3originaldisplayname-canonical-property.md)
    
- [<span data-ttu-id="65d66-134">Propriedade canônica PidLidEmail3OriginalEntryId</span><span class="sxs-lookup"><span data-stu-id="65d66-134">PidLidEmail3OriginalEntryId Canonical Property</span></span>](pidlidemail3originalentryid-canonical-property.md)
    
- [<span data-ttu-id="65d66-135">Propriedade canônica PidLidEmail1DisplayName</span><span class="sxs-lookup"><span data-stu-id="65d66-135">PidLidEmail1DisplayName Canonical Property</span></span>](pidlidemail1displayname-canonical-property.md)
    
- [<span data-ttu-id="65d66-136">Propriedade canônica PidLidEmail1OriginalDisplayName</span><span class="sxs-lookup"><span data-stu-id="65d66-136">PidLidEmail1OriginalDisplayName Canonical Property</span></span>](pidlidemail1originaldisplayname-canonical-property.md)
    
- [<span data-ttu-id="65d66-137">Propriedade canônica PidLidFileUnder</span><span class="sxs-lookup"><span data-stu-id="65d66-137">PidLidFileUnder Canonical Property</span></span>](pidlidfileunder-canonical-property.md)
    
- [<span data-ttu-id="65d66-138">Propriedade canônica PidLidInstantMessagingAddress</span><span class="sxs-lookup"><span data-stu-id="65d66-138">PidLidInstantMessagingAddress Canonical Property</span></span>](pidlidinstantmessagingaddress-canonical-property.md)
    
- [<span data-ttu-id="65d66-139">Propriedade canônica PidLidWorkAddressCity</span><span class="sxs-lookup"><span data-stu-id="65d66-139">PidLidWorkAddressCity Canonical Property</span></span>](pidlidworkaddresscity-canonical-property.md)
    
- [<span data-ttu-id="65d66-140">Propriedade canônica PidLidWorkAddressCountry</span><span class="sxs-lookup"><span data-stu-id="65d66-140">PidLidWorkAddressCountry Canonical Property</span></span>](pidlidworkaddresscountry-canonical-property.md)
    
- [<span data-ttu-id="65d66-141">Propriedade canônica PidLidWorkAddressPostalCode</span><span class="sxs-lookup"><span data-stu-id="65d66-141">PidLidWorkAddressPostalCode Canonical Property</span></span>](pidlidworkaddresspostalcode-canonical-property.md)
    
- [<span data-ttu-id="65d66-142">Propriedade canônica PidLidWorkAddressPostOfficeBox</span><span class="sxs-lookup"><span data-stu-id="65d66-142">PidLidWorkAddressPostOfficeBox Canonical Property</span></span>](pidlidworkaddresspostofficebox-canonical-property.md)
    
- [<span data-ttu-id="65d66-143">Propriedade canônica PidLidWorkAddressState</span><span class="sxs-lookup"><span data-stu-id="65d66-143">PidLidWorkAddressState Canonical Property</span></span>](pidlidworkaddressstate-canonical-property.md)
    
- [<span data-ttu-id="65d66-144">Propriedade canônica PidLidWorkAddressStreet</span><span class="sxs-lookup"><span data-stu-id="65d66-144">PidLidWorkAddressStreet Canonical Property</span></span>](pidlidworkaddressstreet-canonical-property.md)
    
- [<span data-ttu-id="65d66-145">Propriedade canônica PidLidYomiCompanyName</span><span class="sxs-lookup"><span data-stu-id="65d66-145">PidLidYomiCompanyName Canonical Property</span></span>](pidlidyomicompanyname-canonical-property.md)
    
- [<span data-ttu-id="65d66-146">Propriedade canônica PidLidYomiFirstName</span><span class="sxs-lookup"><span data-stu-id="65d66-146">PidLidYomiFirstName Canonical Property</span></span>](pidlidyomifirstname-canonical-property.md)
    
- [<span data-ttu-id="65d66-147">Propriedade canônica PidLidYomiLastName</span><span class="sxs-lookup"><span data-stu-id="65d66-147">PidLidYomiLastName Canonical Property</span></span>](pidlidyomilastname-canonical-property.md)
    
<span data-ttu-id="65d66-148">As propriedades nomeadas no namespace **PSETID_Appointment** são as seguintes:</span><span class="sxs-lookup"><span data-stu-id="65d66-148">Named properties in the **PSETID_Appointment** namespace are the following:</span></span> 
  
- [<span data-ttu-id="65d66-149">Propriedade canônica PidLidAllAttendeesString</span><span class="sxs-lookup"><span data-stu-id="65d66-149">PidLidAllAttendeesString Canonical Property</span></span>](pidlidallattendeesstring-canonical-property.md)
    
- [<span data-ttu-id="65d66-150">Propriedade canônica PidLidAppointmentCounterProposal</span><span class="sxs-lookup"><span data-stu-id="65d66-150">PidLidAppointmentCounterProposal Canonical Property</span></span>](pidlidappointmentcounterproposal-canonical-property.md)
    
- [<span data-ttu-id="65d66-151">Propriedade canônica PidLidAppointmentDuration</span><span class="sxs-lookup"><span data-stu-id="65d66-151">PidLidAppointmentDuration Canonical Property</span></span>](pidlidappointmentduration-canonical-property.md)
    
- [<span data-ttu-id="65d66-152">Propriedade canônica PidLidAppointmentEndWhole</span><span class="sxs-lookup"><span data-stu-id="65d66-152">PidLidAppointmentEndWhole Canonical Property</span></span>](pidlidappointmentendwhole-canonical-property.md)
    
- [<span data-ttu-id="65d66-153">Propriedade canônica PidLidAppointmentStartWhole</span><span class="sxs-lookup"><span data-stu-id="65d66-153">PidLidAppointmentStartWhole Canonical Property</span></span>](pidlidappointmentstartwhole-canonical-property.md)
    
- [<span data-ttu-id="65d66-154">Propriedade canônica PidLidBusyStatus</span><span class="sxs-lookup"><span data-stu-id="65d66-154">PidLidBusyStatus Canonical Property</span></span>](pidlidbusystatus-canonical-property.md)
    
- [<span data-ttu-id="65d66-155">Propriedade canônica PidLidCcAttendeesString</span><span class="sxs-lookup"><span data-stu-id="65d66-155">PidLidCcAttendeesString Canonical Property</span></span>](pidlidccattendeesstring-canonical-property.md)
    
- [<span data-ttu-id="65d66-156">Propriedade canônica PidLidLocation</span><span class="sxs-lookup"><span data-stu-id="65d66-156">PidLidLocation Canonical Property</span></span>](pidlidlocation-canonical-property.md)
    
- [<span data-ttu-id="65d66-157">Propriedade canônica PidLidRecurring</span><span class="sxs-lookup"><span data-stu-id="65d66-157">PidLidRecurring Canonical Property</span></span>](pidlidrecurring-canonical-property.md)
    
- [<span data-ttu-id="65d66-158">Propriedade canônica PidLidToAttendeesString</span><span class="sxs-lookup"><span data-stu-id="65d66-158">PidLidToAttendeesString Canonical Property</span></span>](pidlidtoattendeesstring-canonical-property.md)
    
<span data-ttu-id="65d66-159">As propriedades nomeadas no namespace **PSETID_Common** são as seguintes:</span><span class="sxs-lookup"><span data-stu-id="65d66-159">Named properties in the **PSETID_Common** namespace are the following:</span></span> 
  
- [<span data-ttu-id="65d66-160">Propriedade canônica PidLidCommonEnd</span><span class="sxs-lookup"><span data-stu-id="65d66-160">PidLidCommonEnd Canonical Property</span></span>](pidlidcommonend-canonical-property.md)
    
- [<span data-ttu-id="65d66-161">Propriedade canônica PidLidCommonStart</span><span class="sxs-lookup"><span data-stu-id="65d66-161">PidLidCommonStart Canonical Property</span></span>](pidlidcommonstart-canonical-property.md)
    
- [<span data-ttu-id="65d66-162">Propriedade canônica PidLidCompanies</span><span class="sxs-lookup"><span data-stu-id="65d66-162">PidLidCompanies Canonical Property</span></span>](pidlidcompanies-canonical-property.md)
    
- [<span data-ttu-id="65d66-163">Propriedade canônica PidLidContacts</span><span class="sxs-lookup"><span data-stu-id="65d66-163">PidLidContacts Canonical Property</span></span>](pidlidcontacts-canonical-property.md)
    
- [<span data-ttu-id="65d66-164">Propriedade canônica PidLidCustomFlag</span><span class="sxs-lookup"><span data-stu-id="65d66-164">PidLidCustomFlag Canonical Property</span></span>](pidlidcustomflag-canonical-property.md)
    
- [<span data-ttu-id="65d66-165">Propriedade canônica PidLidFormPropStream</span><span class="sxs-lookup"><span data-stu-id="65d66-165">PidLidFormPropStream Canonical Property</span></span>](pidlidformpropstream-canonical-property.md)
    
- [<span data-ttu-id="65d66-166">Propriedade canônica PidLidFormStorage</span><span class="sxs-lookup"><span data-stu-id="65d66-166">PidLidFormStorage Canonical Property</span></span>](pidlidformstorage-canonical-property.md)
    
- [<span data-ttu-id="65d66-167">Propriedade canônica PidLidHeaderItem</span><span class="sxs-lookup"><span data-stu-id="65d66-167">PidLidHeaderItem Canonical Property</span></span>](pidlidheaderitem-canonical-property.md)
    
- [<span data-ttu-id="65d66-168">Propriedade canônica PidLidPageDirStream</span><span class="sxs-lookup"><span data-stu-id="65d66-168">PidLidPageDirStream Canonical Property</span></span>](pidlidpagedirstream-canonical-property.md)
    
- [<span data-ttu-id="65d66-169">Propriedade canônica PidLidPropertyDefinitionStream</span><span class="sxs-lookup"><span data-stu-id="65d66-169">PidLidPropertyDefinitionStream Canonical Property</span></span>](pidlidpropertydefinitionstream-canonical-property.md)
    
- [<span data-ttu-id="65d66-170">Propriedade canônica PidLidReminderSet</span><span class="sxs-lookup"><span data-stu-id="65d66-170">PidLidReminderSet Canonical Property</span></span>](pidlidreminderset-canonical-property.md)
    
- [<span data-ttu-id="65d66-171">Propriedade canônica PidLidReminderTime</span><span class="sxs-lookup"><span data-stu-id="65d66-171">PidLidReminderTime Canonical Property</span></span>](pidlidremindertime-canonical-property.md)
    
- [<span data-ttu-id="65d66-172">Propriedade canônica PidLidFlagRequest</span><span class="sxs-lookup"><span data-stu-id="65d66-172">PidLidFlagRequest Canonical Property</span></span>](pidlidflagrequest-canonical-property.md)
    
- [<span data-ttu-id="65d66-173">Propriedade canônica PidLidScriptStream</span><span class="sxs-lookup"><span data-stu-id="65d66-173">PidLidScriptStream Canonical Property</span></span>](pidlidscriptstream-canonical-property.md)
    
- [<span data-ttu-id="65d66-174">Propriedade canônica PidLidSmartNoAttach</span><span class="sxs-lookup"><span data-stu-id="65d66-174">PidLidSmartNoAttach Canonical Property</span></span>](pidlidsmartnoattach-canonical-property.md)
    
- [<span data-ttu-id="65d66-175">Propriedade canônica PidLidToDoTitle</span><span class="sxs-lookup"><span data-stu-id="65d66-175">PidLidToDoTitle Canonical Property</span></span>](pidlidtodotitle-canonical-property.md)
    
- [<span data-ttu-id="65d66-176">Propriedade canônica PidLidUseTnef</span><span class="sxs-lookup"><span data-stu-id="65d66-176">PidLidUseTnef Canonical Property</span></span>](pidlidusetnef-canonical-property.md)
    
<span data-ttu-id="65d66-177">As propriedades nomeadas no namespace **PSETID_Meeting** são as seguintes:</span><span class="sxs-lookup"><span data-stu-id="65d66-177">Named properties in the **PSETID_Meeting** namespace are the following:</span></span> 
  
- [<span data-ttu-id="65d66-178">Propriedade canônica PidLidMeetingType</span><span class="sxs-lookup"><span data-stu-id="65d66-178">PidLidMeetingType Canonical Property</span></span>](pidlidmeetingtype-canonical-property.md)
    
<span data-ttu-id="65d66-179">As propriedades nomeadas no namespace **PSETID_Task** são as seguintes:</span><span class="sxs-lookup"><span data-stu-id="65d66-179">Named properties in the **PSETID_Task** namespace are the following:</span></span> 
  
- [<span data-ttu-id="65d66-180">Propriedade canônica PidLidTaskActualEffort</span><span class="sxs-lookup"><span data-stu-id="65d66-180">PidLidTaskActualEffort Canonical Property</span></span>](pidlidtaskactualeffort-canonical-property.md)
    
- [<span data-ttu-id="65d66-181">Propriedade canônica PidLidTaskDueDate</span><span class="sxs-lookup"><span data-stu-id="65d66-181">PidLidTaskDueDate Canonical Property</span></span>](pidlidtaskduedate-canonical-property.md)
    
- [<span data-ttu-id="65d66-182">Propriedade canônica PidLidTaskEstimatedEffort</span><span class="sxs-lookup"><span data-stu-id="65d66-182">PidLidTaskEstimatedEffort Canonical Property</span></span>](pidlidtaskestimatedeffort-canonical-property.md)
    
- [<span data-ttu-id="65d66-183">Propriedade canônica PidLidTaskFRecurring</span><span class="sxs-lookup"><span data-stu-id="65d66-183">PidLidTaskFRecurring Canonical Property</span></span>](pidlidtaskfrecurring-canonical-property.md)
    
- [<span data-ttu-id="65d66-184">Propriedade canônica PidLidTaskStartDate</span><span class="sxs-lookup"><span data-stu-id="65d66-184">PidLidTaskStartDate Canonical Property</span></span>](pidlidtaskstartdate-canonical-property.md)
    
- [<span data-ttu-id="65d66-185">Propriedade canônica PidLidTaskStatus</span><span class="sxs-lookup"><span data-stu-id="65d66-185">PidLidTaskStatus Canonical Property</span></span>](pidlidtaskstatus-canonical-property.md)
    
<span data-ttu-id="65d66-186">As propriedades nomeadas no namespace **PS_INTERNET_HEADERS** são as seguintes:</span><span class="sxs-lookup"><span data-stu-id="65d66-186">Named properties in the **PS_INTERNET_HEADERS** namespace are the following:</span></span> 
  
- [<span data-ttu-id="65d66-187">Propriedade canônica PidTagInternetReturnPath</span><span class="sxs-lookup"><span data-stu-id="65d66-187">PidTagInternetReturnPath Canonical Property</span></span>](pidtaginternetreturnpath-canonical-property.md)
    
<span data-ttu-id="65d66-188">As propriedades nomeadas no namespace **PSETID_Log** são as seguintes:</span><span class="sxs-lookup"><span data-stu-id="65d66-188">Named properties in the **PSETID_Log** namespace are the following:</span></span> 
  
- [<span data-ttu-id="65d66-189">Propriedade canônica PidLidLogDuration</span><span class="sxs-lookup"><span data-stu-id="65d66-189">PidLidLogDuration Canonical Property</span></span>](pidlidlogduration-canonical-property.md)
    
- [<span data-ttu-id="65d66-190">Propriedade canônica PidLidLogEnd</span><span class="sxs-lookup"><span data-stu-id="65d66-190">PidLidLogEnd Canonical Property</span></span>](pidlidlogend-canonical-property.md)
    
- [<span data-ttu-id="65d66-191">Propriedade canônica PidLidLogStart</span><span class="sxs-lookup"><span data-stu-id="65d66-191">PidLidLogStart Canonical Property</span></span>](pidlidlogstart-canonical-property.md)
    
- [<span data-ttu-id="65d66-192">Propriedade canônica PidLidLogType</span><span class="sxs-lookup"><span data-stu-id="65d66-192">PidLidLogType Canonical Property</span></span>](pidlidlogtype-canonical-property.md)
    
<span data-ttu-id="65d66-193">As propriedades nomeadas no namespace **PSETID_PUBLIC_STRINGS** são as seguintes:</span><span class="sxs-lookup"><span data-stu-id="65d66-193">Named properties in the **PS_PUBLIC_STRINGS** namespace are the following:</span></span> 
  
- [<span data-ttu-id="65d66-194">Propriedade canônica PidNameKeywords</span><span class="sxs-lookup"><span data-stu-id="65d66-194">PidNameKeywords Canonical Property</span></span>](pidnamekeywords-canonical-property.md)
    
- [<span data-ttu-id="65d66-195">Propriedade canônica PidNameExchangeJunkEmailMoveStamp</span><span class="sxs-lookup"><span data-stu-id="65d66-195">PidNameExchangeJunkEmailMoveStamp Canonical Property</span></span>](pidnameexchangejunkemailmovestamp-canonical-property.md)
    
## <a name="see-also"></a><span data-ttu-id="65d66-196">Confira também</span><span class="sxs-lookup"><span data-stu-id="65d66-196">See also</span></span>



[<span data-ttu-id="65d66-197">Constantes de MAPI</span><span class="sxs-lookup"><span data-stu-id="65d66-197">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="65d66-198">Determinar se o Outlook baixou somente o cabeçalho de uma mensagem</span><span class="sxs-lookup"><span data-stu-id="65d66-198">Determine if Outlook Downloaded Only the Header of a Message</span></span>](how-to-determine-if-outlook-downloaded-only-the-header-of-a-message.md)
  
[<span data-ttu-id="65d66-199">Obter o endereço de email de um item de contato</span><span class="sxs-lookup"><span data-stu-id="65d66-199">Get the Email Address of a Contact Item</span></span>](how-to-get-the-email-address-of-a-contact-item.md)
  
[<span data-ttu-id="65d66-200">Remover a definição de formulário personalizada salva com uma mensagem</span><span class="sxs-lookup"><span data-stu-id="65d66-200">Remove Custom Form Definition Saved With a Message</span></span>](how-to-remove-custom-form-definition-saved-with-a-message.md)

