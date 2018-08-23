---
title: Sobre propriedades nomeadas usadas pelo Outlook
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 8c245ec2-bb18-ecf0-b4ad-8c164c5924cf
description: '�ltima altera��o: segunda-feira, 25 de junho de 2012'
ms.openlocfilehash: aa4d52d25f120e8b3e2a4c0dcaa4845ad576127a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566226"
---
# <a name="about-named-properties-used-by-outlook"></a><span data-ttu-id="c6c37-103">Sobre propriedades nomeadas usadas pelo Outlook</span><span class="sxs-lookup"><span data-stu-id="c6c37-103">About Named Properties Used by Outlook</span></span>

  
  
<span data-ttu-id="c6c37-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c6c37-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c6c37-p101">MAPI fornece uma facilidade para atribuir nomes para determinadas propriedades para mapear esses nomes para identificadores exclusivos e para tornar os esse nome-para-identificador mapeamento persistente entre sess�es. Propriedades nomeadas s�o identificadas por um nome e um identificador global exclusivo (GUID) para um conjunto de propriedades. O nome pode ser um n�mero ou uma cadeia de caracteres. Para Microsoft Outlook 2013 ou Microsoft Outlook 2010, o conjunto de propriedades � geralmente um namespace definido por Outlook�2013 ou Outlook�2010, como **PSETID_Appointment**.</span><span class="sxs-lookup"><span data-stu-id="c6c37-p101">MAPI provides a facility for assigning names to certain properties, for mapping these names to unique identifiers, and for making this name-to-identifier mapping persistent across sessions. Named properties are identified by a name and a globally unique identifier (GUID) for a property set. The name can be a number or a string. For Microsoft Outlook 2013 or Microsoft Outlook 2010, the property set is often a namespace defined by Outlook 2013 or Outlook 2010, such as **PSETID_Appointment**.</span></span> 
  
<span data-ttu-id="c6c37-p102">Named properties are manipulated by using the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) function and the [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) function. The name and the property set GUID are passed to the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) function to obtain a property identifier that is valid for the current MAPI session. Because this property identifier can vary from computer to computer, the only consistent way to access a named property is to know its name and property set GUID. The range for identifiers is always in the 0x8000 and 0xFFFE range.</span><span class="sxs-lookup"><span data-stu-id="c6c37-p102">Named properties are manipulated by using the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) function and the [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) function. The name and the property set GUID are passed to the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) function to obtain a property identifier that is valid for the current MAPI session. Because this property identifier can vary from computer to computer, the only consistent way to access a named property is to know its name and property set GUID. The range for identifiers is always in the 0x8000 and 0xFFFE range.</span></span> 
  
<span data-ttu-id="c6c37-p103">Any object that implements the [IMAPIProp: IUnknown](imapipropiunknown.md) interface can support named properties. Specifically, a MAPI service provider or a MAPI client must implement [IMAPIProp::GetProps](imapiprop-getprops.md) to get values of named properties. Setting named properties used by Outlook�2013 or Outlook�2010 is not supported because of the risk of corrupting data that is shared with other MAPI providers or clients.</span><span class="sxs-lookup"><span data-stu-id="c6c37-p103">Any object that implements the [IMAPIProp : IUnknown](imapipropiunknown.md) interface can support named properties. Specifically, a MAPI service provider or a MAPI client must implement [IMAPIProp::GetProps](imapiprop-getprops.md) to get values of named properties. Setting named properties used by Outlook 2013 or Outlook 2010 is not supported because of the risk of corrupting data that is shared with other MAPI providers or clients.</span></span> 
  
<span data-ttu-id="c6c37-p104">Outlook�2013 and Outlook�2010 use MAPI named properties to implement many of their features, for example, attachment security and meeting counter-proposals. Above this underlying data, Outlook�2013 and Outlook�2010 expose some of these properties as item properties in their Outlook�2013 and Outlook�2010 object models. For example, the **Email1Address** property of the **ContactItem** object in the object model corresponds to the named [Propriedade can�nico de PidLidEmail1EmailAddress](pidlidemail1emailaddress-canonical-property.md) in the **PSETID_Address** namespace. But in general, due to concerns for compatibility and data integrity, many of the MAPI properties that are used by Outlook�2013 and Outlook�2010 are not exposed in the object model.</span><span class="sxs-lookup"><span data-stu-id="c6c37-p104">Outlook 2013 and Outlook 2010 use MAPI named properties to implement many of their features, for example, attachment security and meeting counter-proposals. Above this underlying data, Outlook 2013 and Outlook 2010 expose some of these properties as item properties in their Outlook 2013 and Outlook 2010 object models. For example, the **Email1Address** property of the **ContactItem** object in the object model corresponds to the named [PidLidEmail1EmailAddress Canonical Property](pidlidemail1emailaddress-canonical-property.md) in the **PSETID_Address** namespace. But in general, due to concerns for compatibility and data integrity, many of the MAPI properties that are used by Outlook 2013 and Outlook 2010 are not exposed in the object model.</span></span> 
  
<span data-ttu-id="c6c37-120">Esta refer�ncia descreve um n�mero de propriedades nomeadas listadas abaixo.</span><span class="sxs-lookup"><span data-stu-id="c6c37-120">This reference describes a number of named properties that are listed below.</span></span>
  
<span data-ttu-id="c6c37-121">Propriedades nomeadas no namespace **PSETID_Address** s�o as seguintes:</span><span class="sxs-lookup"><span data-stu-id="c6c37-121">Named properties in the **PSETID_Address** namespace are the following:</span></span> 
  
- [<span data-ttu-id="c6c37-122">Propriedade can�nico de PidLidEmail1AddressType</span><span class="sxs-lookup"><span data-stu-id="c6c37-122">PidLidEmail1AddressType Canonical Property</span></span>](pidlidemail1addresstype-canonical-property.md)
    
- [<span data-ttu-id="c6c37-123">Propriedade can�nico de PidLidEmail1EmailAddress</span><span class="sxs-lookup"><span data-stu-id="c6c37-123">PidLidEmail1EmailAddress Canonical Property</span></span>](pidlidemail1emailaddress-canonical-property.md)
    
- [<span data-ttu-id="c6c37-124">Propriedade can�nico de PidLidEmail1OriginalEntryId</span><span class="sxs-lookup"><span data-stu-id="c6c37-124">PidLidEmail1OriginalEntryId Canonical Property</span></span>](pidlidemail1originalentryid-canonical-property.md)
    
- [<span data-ttu-id="c6c37-125">Propriedade can�nico de PidLidEmail2AddressType</span><span class="sxs-lookup"><span data-stu-id="c6c37-125">PidLidEmail2AddressType Canonical Property</span></span>](pidlidemail2addresstype-canonical-property.md)
    
- [<span data-ttu-id="c6c37-126">Propriedade can�nico de PidLidEmail2DisplayName</span><span class="sxs-lookup"><span data-stu-id="c6c37-126">PidLidEmail2DisplayName Canonical Property</span></span>](pidlidemail2displayname-canonical-property.md)
    
- [<span data-ttu-id="c6c37-127">Propriedade can�nico de PidLidEmail2EmailAddress</span><span class="sxs-lookup"><span data-stu-id="c6c37-127">PidLidEmail2EmailAddress Canonical Property</span></span>](pidlidemail2emailaddress-canonical-property.md)
    
- [<span data-ttu-id="c6c37-128">Propriedade can�nico de PidLidEmail2OriginalDisplayName</span><span class="sxs-lookup"><span data-stu-id="c6c37-128">PidLidEmail2OriginalDisplayName Canonical Property</span></span>](pidlidemail2originaldisplayname-canonical-property.md)
    
- [<span data-ttu-id="c6c37-129">Propriedade can�nico de PidLidEmail2OriginalEntryId</span><span class="sxs-lookup"><span data-stu-id="c6c37-129">PidLidEmail2OriginalEntryId Canonical Property</span></span>](pidlidemail2originalentryid-canonical-property.md)
    
- [<span data-ttu-id="c6c37-130">Propriedade can�nico de PidLidEmail3AddressType</span><span class="sxs-lookup"><span data-stu-id="c6c37-130">PidLidEmail3AddressType Canonical Property</span></span>](pidlidemail3addresstype-canonical-property.md)
    
- [<span data-ttu-id="c6c37-131">Propriedade can�nico de PidLidEmail3DisplayName</span><span class="sxs-lookup"><span data-stu-id="c6c37-131">PidLidEmail3DisplayName Canonical Property</span></span>](pidlidemail3displayname-canonical-property.md)
    
- [<span data-ttu-id="c6c37-132">Propriedade can�nico de PidLidEmail3EmailAddress</span><span class="sxs-lookup"><span data-stu-id="c6c37-132">PidLidEmail3EmailAddress Canonical Property</span></span>](pidlidemail3emailaddress-canonical-property.md)
    
- [<span data-ttu-id="c6c37-133">Propriedade can�nico de PidLidEmail3OriginalDisplayName</span><span class="sxs-lookup"><span data-stu-id="c6c37-133">PidLidEmail3OriginalDisplayName Canonical Property</span></span>](pidlidemail3originaldisplayname-canonical-property.md)
    
- [<span data-ttu-id="c6c37-134">Propriedade can�nico de PidLidEmail3OriginalEntryId</span><span class="sxs-lookup"><span data-stu-id="c6c37-134">PidLidEmail3OriginalEntryId Canonical Property</span></span>](pidlidemail3originalentryid-canonical-property.md)
    
- [<span data-ttu-id="c6c37-135">Propriedade can�nico de PidLidEmail1DisplayName</span><span class="sxs-lookup"><span data-stu-id="c6c37-135">PidLidEmail1DisplayName Canonical Property</span></span>](pidlidemail1displayname-canonical-property.md)
    
- [<span data-ttu-id="c6c37-136">Propriedade can�nico de PidLidEmail1OriginalDisplayName</span><span class="sxs-lookup"><span data-stu-id="c6c37-136">PidLidEmail1OriginalDisplayName Canonical Property</span></span>](pidlidemail1originaldisplayname-canonical-property.md)
    
- [<span data-ttu-id="c6c37-137">Propriedade can�nico de PidLidFileUnder</span><span class="sxs-lookup"><span data-stu-id="c6c37-137">PidLidFileUnder Canonical Property</span></span>](pidlidfileunder-canonical-property.md)
    
- [<span data-ttu-id="c6c37-138">Propriedade can�nico de PidLidInstantMessagingAddress</span><span class="sxs-lookup"><span data-stu-id="c6c37-138">PidLidInstantMessagingAddress Canonical Property</span></span>](pidlidinstantmessagingaddress-canonical-property.md)
    
- [<span data-ttu-id="c6c37-139">Propriedade can�nico de PidLidWorkAddressCity</span><span class="sxs-lookup"><span data-stu-id="c6c37-139">PidLidWorkAddressCity Canonical Property</span></span>](pidlidworkaddresscity-canonical-property.md)
    
- [<span data-ttu-id="c6c37-140">Propriedade can�nico de PidLidWorkAddressCountry</span><span class="sxs-lookup"><span data-stu-id="c6c37-140">PidLidWorkAddressCountry Canonical Property</span></span>](pidlidworkaddresscountry-canonical-property.md)
    
- [<span data-ttu-id="c6c37-141">Propriedade can�nico de PidLidWorkAddressPostalCode</span><span class="sxs-lookup"><span data-stu-id="c6c37-141">PidLidWorkAddressPostalCode Canonical Property</span></span>](pidlidworkaddresspostalcode-canonical-property.md)
    
- [<span data-ttu-id="c6c37-142">Propriedade can�nico de PidLidWorkAddressPostOfficeBox</span><span class="sxs-lookup"><span data-stu-id="c6c37-142">PidLidWorkAddressPostOfficeBox Canonical Property</span></span>](pidlidworkaddresspostofficebox-canonical-property.md)
    
- [<span data-ttu-id="c6c37-143">Propriedade can�nico de PidLidWorkAddressState</span><span class="sxs-lookup"><span data-stu-id="c6c37-143">PidLidWorkAddressState Canonical Property</span></span>](pidlidworkaddressstate-canonical-property.md)
    
- [<span data-ttu-id="c6c37-144">Propriedade can�nico de PidLidWorkAddressStreet</span><span class="sxs-lookup"><span data-stu-id="c6c37-144">PidLidWorkAddressStreet Canonical Property</span></span>](pidlidworkaddressstreet-canonical-property.md)
    
- [<span data-ttu-id="c6c37-145">Propriedade can�nico de PidLidYomiCompanyName</span><span class="sxs-lookup"><span data-stu-id="c6c37-145">PidLidYomiCompanyName Canonical Property</span></span>](pidlidyomicompanyname-canonical-property.md)
    
- [<span data-ttu-id="c6c37-146">Propriedade can�nico de PidLidYomiFirstName</span><span class="sxs-lookup"><span data-stu-id="c6c37-146">PidLidYomiFirstName Canonical Property</span></span>](pidlidyomifirstname-canonical-property.md)
    
- [<span data-ttu-id="c6c37-147">Propriedade can�nico de PidLidYomiLastName</span><span class="sxs-lookup"><span data-stu-id="c6c37-147">PidLidYomiLastName Canonical Property</span></span>](pidlidyomilastname-canonical-property.md)
    
<span data-ttu-id="c6c37-148">Propriedades nomeadas no namespace **PSETID_Appointment** s�o as seguintes:</span><span class="sxs-lookup"><span data-stu-id="c6c37-148">Named properties in the **PSETID_Appointment** namespace are the following:</span></span> 
  
- [<span data-ttu-id="c6c37-149">Propriedade can�nico de PidLidAllAttendeesString</span><span class="sxs-lookup"><span data-stu-id="c6c37-149">PidLidAllAttendeesString Canonical Property</span></span>](pidlidallattendeesstring-canonical-property.md)
    
- [<span data-ttu-id="c6c37-150">Propriedade can�nico de PidLidAppointmentCounterProposal</span><span class="sxs-lookup"><span data-stu-id="c6c37-150">PidLidAppointmentCounterProposal Canonical Property</span></span>](pidlidappointmentcounterproposal-canonical-property.md)
    
- [<span data-ttu-id="c6c37-151">Propriedade can�nico de PidLidAppointmentDuration</span><span class="sxs-lookup"><span data-stu-id="c6c37-151">PidLidAppointmentDuration Canonical Property</span></span>](pidlidappointmentduration-canonical-property.md)
    
- [<span data-ttu-id="c6c37-152">Propriedade can�nico de PidLidAppointmentEndWhole</span><span class="sxs-lookup"><span data-stu-id="c6c37-152">PidLidAppointmentEndWhole Canonical Property</span></span>](pidlidappointmentendwhole-canonical-property.md)
    
- [<span data-ttu-id="c6c37-153">Propriedade can�nico de PidLidAppointmentStartWhole</span><span class="sxs-lookup"><span data-stu-id="c6c37-153">PidLidAppointmentStartWhole Canonical Property</span></span>](pidlidappointmentstartwhole-canonical-property.md)
    
- [<span data-ttu-id="c6c37-154">Propriedade can�nico de PidLidBusyStatus</span><span class="sxs-lookup"><span data-stu-id="c6c37-154">PidLidBusyStatus Canonical Property</span></span>](pidlidbusystatus-canonical-property.md)
    
- [<span data-ttu-id="c6c37-155">Propriedade can�nico de PidLidCcAttendeesString</span><span class="sxs-lookup"><span data-stu-id="c6c37-155">PidLidCcAttendeesString Canonical Property</span></span>](pidlidccattendeesstring-canonical-property.md)
    
- [<span data-ttu-id="c6c37-156">Propriedade can�nico de PidLidLocation</span><span class="sxs-lookup"><span data-stu-id="c6c37-156">PidLidLocation Canonical Property</span></span>](pidlidlocation-canonical-property.md)
    
- [<span data-ttu-id="c6c37-157">Propriedade can�nico de PidLidRecurring</span><span class="sxs-lookup"><span data-stu-id="c6c37-157">PidLidRecurring Canonical Property</span></span>](pidlidrecurring-canonical-property.md)
    
- [<span data-ttu-id="c6c37-158">Propriedade can�nico de PidLidToAttendeesString</span><span class="sxs-lookup"><span data-stu-id="c6c37-158">PidLidToAttendeesString Canonical Property</span></span>](pidlidtoattendeesstring-canonical-property.md)
    
<span data-ttu-id="c6c37-159">Propriedades nomeadas no namespace **PSETID_Common** s�o as seguintes:</span><span class="sxs-lookup"><span data-stu-id="c6c37-159">Named properties in the **PSETID_Common** namespace are the following:</span></span> 
  
- [<span data-ttu-id="c6c37-160">Propriedade can�nico de PidLidCommonEnd</span><span class="sxs-lookup"><span data-stu-id="c6c37-160">PidLidCommonEnd Canonical Property</span></span>](pidlidcommonend-canonical-property.md)
    
- [<span data-ttu-id="c6c37-161">Propriedade can�nico de PidLidCommonStart</span><span class="sxs-lookup"><span data-stu-id="c6c37-161">PidLidCommonStart Canonical Property</span></span>](pidlidcommonstart-canonical-property.md)
    
- [<span data-ttu-id="c6c37-162">Propriedade can�nico de PidLidCompanies</span><span class="sxs-lookup"><span data-stu-id="c6c37-162">PidLidCompanies Canonical Property</span></span>](pidlidcompanies-canonical-property.md)
    
- [<span data-ttu-id="c6c37-163">Propriedade can�nico de PidLidContacts</span><span class="sxs-lookup"><span data-stu-id="c6c37-163">PidLidContacts Canonical Property</span></span>](pidlidcontacts-canonical-property.md)
    
- [<span data-ttu-id="c6c37-164">Propriedade can�nico de PidLidCustomFlag</span><span class="sxs-lookup"><span data-stu-id="c6c37-164">PidLidCustomFlag Canonical Property</span></span>](pidlidcustomflag-canonical-property.md)
    
- [<span data-ttu-id="c6c37-165">Propriedade can�nico de PidLidFormPropStream</span><span class="sxs-lookup"><span data-stu-id="c6c37-165">PidLidFormPropStream Canonical Property</span></span>](pidlidformpropstream-canonical-property.md)
    
- [<span data-ttu-id="c6c37-166">Propriedade can�nico de PidLidFormStorage</span><span class="sxs-lookup"><span data-stu-id="c6c37-166">PidLidFormStorage Canonical Property</span></span>](pidlidformstorage-canonical-property.md)
    
- [<span data-ttu-id="c6c37-167">Propriedade can�nico de PidLidHeaderItem</span><span class="sxs-lookup"><span data-stu-id="c6c37-167">PidLidHeaderItem Canonical Property</span></span>](pidlidheaderitem-canonical-property.md)
    
- [<span data-ttu-id="c6c37-168">Propriedade can�nico de PidLidPageDirStream</span><span class="sxs-lookup"><span data-stu-id="c6c37-168">PidLidPageDirStream Canonical Property</span></span>](pidlidpagedirstream-canonical-property.md)
    
- [<span data-ttu-id="c6c37-169">Propriedade can�nico de PidLidPropertyDefinitionStream</span><span class="sxs-lookup"><span data-stu-id="c6c37-169">PidLidPropertyDefinitionStream Canonical Property</span></span>](pidlidpropertydefinitionstream-canonical-property.md)
    
- [<span data-ttu-id="c6c37-170">Propriedade can�nico de PidLidReminderSet</span><span class="sxs-lookup"><span data-stu-id="c6c37-170">PidLidReminderSet Canonical Property</span></span>](pidlidreminderset-canonical-property.md)
    
- [<span data-ttu-id="c6c37-171">Propriedade can�nico de PidLidReminderTime</span><span class="sxs-lookup"><span data-stu-id="c6c37-171">PidLidReminderTime Canonical Property</span></span>](pidlidremindertime-canonical-property.md)
    
- [<span data-ttu-id="c6c37-172">Propriedade can�nico de PidLidFlagRequest</span><span class="sxs-lookup"><span data-stu-id="c6c37-172">PidLidFlagRequest Canonical Property</span></span>](pidlidflagrequest-canonical-property.md)
    
- [<span data-ttu-id="c6c37-173">Propriedade can�nico de PidLidScriptStream</span><span class="sxs-lookup"><span data-stu-id="c6c37-173">PidLidScriptStream Canonical Property</span></span>](pidlidscriptstream-canonical-property.md)
    
- [<span data-ttu-id="c6c37-174">Propriedade can�nico de PidLidSmartNoAttach</span><span class="sxs-lookup"><span data-stu-id="c6c37-174">PidLidSmartNoAttach Canonical Property</span></span>](pidlidsmartnoattach-canonical-property.md)
    
- [<span data-ttu-id="c6c37-175">Propriedade can�nico de PidLidToDoTitle</span><span class="sxs-lookup"><span data-stu-id="c6c37-175">PidLidToDoTitle Canonical Property</span></span>](pidlidtodotitle-canonical-property.md)
    
- [<span data-ttu-id="c6c37-176">Propriedade can�nico de PidLidUseTnef</span><span class="sxs-lookup"><span data-stu-id="c6c37-176">PidLidUseTnef Canonical Property</span></span>](pidlidusetnef-canonical-property.md)
    
<span data-ttu-id="c6c37-177">Propriedades nomeadas no namespace **PSETID_Meeting** s�o as seguintes:</span><span class="sxs-lookup"><span data-stu-id="c6c37-177">Named properties in the **PSETID_Meeting** namespace are the following:</span></span> 
  
- [<span data-ttu-id="c6c37-178">Propriedade can�nico de PidLidMeetingType</span><span class="sxs-lookup"><span data-stu-id="c6c37-178">PidLidMeetingType Canonical Property</span></span>](pidlidmeetingtype-canonical-property.md)
    
<span data-ttu-id="c6c37-179">Propriedades nomeadas no namespace **PSETID_Task** s�o as seguintes:</span><span class="sxs-lookup"><span data-stu-id="c6c37-179">Named properties in the **PSETID_Task** namespace are the following:</span></span> 
  
- [<span data-ttu-id="c6c37-180">Propriedade can�nico de PidLidTaskActualEffort</span><span class="sxs-lookup"><span data-stu-id="c6c37-180">PidLidTaskActualEffort Canonical Property</span></span>](pidlidtaskactualeffort-canonical-property.md)
    
- [<span data-ttu-id="c6c37-181">Propriedade can�nico de PidLidTaskDueDate</span><span class="sxs-lookup"><span data-stu-id="c6c37-181">PidLidTaskDueDate Canonical Property</span></span>](pidlidtaskduedate-canonical-property.md)
    
- [<span data-ttu-id="c6c37-182">Propriedade can�nico de PidLidTaskEstimatedEffort</span><span class="sxs-lookup"><span data-stu-id="c6c37-182">PidLidTaskEstimatedEffort Canonical Property</span></span>](pidlidtaskestimatedeffort-canonical-property.md)
    
- [<span data-ttu-id="c6c37-183">Propriedade can�nico de PidLidTaskFRecurring</span><span class="sxs-lookup"><span data-stu-id="c6c37-183">PidLidTaskFRecurring Canonical Property</span></span>](pidlidtaskfrecurring-canonical-property.md)
    
- [<span data-ttu-id="c6c37-184">Propriedade can�nico de PidLidTaskStartDate</span><span class="sxs-lookup"><span data-stu-id="c6c37-184">PidLidTaskStartDate Canonical Property</span></span>](pidlidtaskstartdate-canonical-property.md)
    
- [<span data-ttu-id="c6c37-185">Propriedade can�nico de PidLidTaskStatus</span><span class="sxs-lookup"><span data-stu-id="c6c37-185">PidLidTaskStatus Canonical Property</span></span>](pidlidtaskstatus-canonical-property.md)
    
<span data-ttu-id="c6c37-186">Propriedades nomeadas no namespace **PS_INTERNET_HEADERS** s�o as seguintes:</span><span class="sxs-lookup"><span data-stu-id="c6c37-186">Named properties in the **PS_INTERNET_HEADERS** namespace are the following:</span></span> 
  
- [<span data-ttu-id="c6c37-187">Propriedade can�nico de PidTagInternetReturnPath</span><span class="sxs-lookup"><span data-stu-id="c6c37-187">PidTagInternetReturnPath Canonical Property</span></span>](pidtaginternetreturnpath-canonical-property.md)
    
<span data-ttu-id="c6c37-188">Propriedades nomeadas no namespace **PSETID_Log** s�o as seguintes:</span><span class="sxs-lookup"><span data-stu-id="c6c37-188">Named properties in the **PSETID_Log** namespace are the following:</span></span> 
  
- [<span data-ttu-id="c6c37-189">Propriedade can�nico de PidLidLogDuration</span><span class="sxs-lookup"><span data-stu-id="c6c37-189">PidLidLogDuration Canonical Property</span></span>](pidlidlogduration-canonical-property.md)
    
- [<span data-ttu-id="c6c37-190">Propriedade can�nico de PidLidLogEnd</span><span class="sxs-lookup"><span data-stu-id="c6c37-190">PidLidLogEnd Canonical Property</span></span>](pidlidlogend-canonical-property.md)
    
- [<span data-ttu-id="c6c37-191">Propriedade can�nico de PidLidLogStart</span><span class="sxs-lookup"><span data-stu-id="c6c37-191">PidLidLogStart Canonical Property</span></span>](pidlidlogstart-canonical-property.md)
    
- [<span data-ttu-id="c6c37-192">Propriedade can�nico de PidLidLogType</span><span class="sxs-lookup"><span data-stu-id="c6c37-192">PidLidLogType Canonical Property</span></span>](pidlidlogtype-canonical-property.md)
    
<span data-ttu-id="c6c37-193">Propriedades nomeadas no namespace **PS_PUBLIC_STRINGS** s�o as seguintes:</span><span class="sxs-lookup"><span data-stu-id="c6c37-193">Named properties in the **PS_PUBLIC_STRINGS** namespace are the following:</span></span> 
  
- [<span data-ttu-id="c6c37-194">Propriedade can�nico de PidNameKeywords</span><span class="sxs-lookup"><span data-stu-id="c6c37-194">PidNameKeywords Canonical Property</span></span>](pidnamekeywords-canonical-property.md)
    
- [<span data-ttu-id="c6c37-195">Propriedade can�nico de PidNameExchangeJunkEmailMoveStamp</span><span class="sxs-lookup"><span data-stu-id="c6c37-195">PidNameExchangeJunkEmailMoveStamp Canonical Property</span></span>](pidnameexchangejunkemailmovestamp-canonical-property.md)
    
## <a name="see-also"></a><span data-ttu-id="c6c37-196">Ver tamb�m</span><span class="sxs-lookup"><span data-stu-id="c6c37-196">See also</span></span>



[<span data-ttu-id="c6c37-197">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="c6c37-197">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="c6c37-198">Determinar se o Outlook baixou somente o cabeçalho de uma mensagem</span><span class="sxs-lookup"><span data-stu-id="c6c37-198">Determine if Outlook Downloaded Only the Header of a Message</span></span>](how-to-determine-if-outlook-downloaded-only-the-header-of-a-message.md)
  
[<span data-ttu-id="c6c37-199">Obter o endereço de Email de um item de contato</span><span class="sxs-lookup"><span data-stu-id="c6c37-199">Get the Email Address of a Contact Item</span></span>](how-to-get-the-email-address-of-a-contact-item.md)
  
[<span data-ttu-id="c6c37-200">Remover a definição de formulário personalizada salva com uma mensagem</span><span class="sxs-lookup"><span data-stu-id="c6c37-200">Remove Custom Form Definition Saved With a Message</span></span>](how-to-remove-custom-form-definition-saved-with-a-message.md)

