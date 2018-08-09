---
title: Sobre propriedades nomeadas usadas pelo Outlook
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 8c245ec2-bb18-ecf0-b4ad-8c164c5924cf
description: '�ltima altera��o: segunda-feira, 25 de junho de 2012'
ms.openlocfilehash: 75a08db313ac1b38a400fb329eefa914858ec71e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766092"
---
# <a name="about-named-properties-used-by-outlook"></a><span data-ttu-id="dbd5a-103">Sobre propriedades nomeadas usadas pelo Outlook</span><span class="sxs-lookup"><span data-stu-id="dbd5a-103">About Named Properties Used by Outlook</span></span>

  
  
<span data-ttu-id="dbd5a-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="dbd5a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="dbd5a-p101">MAPI fornece uma facilidade para atribuir nomes para determinadas propriedades para mapear esses nomes para identificadores exclusivos e para tornar os esse nome-para-identificador mapeamento persistente entre sess�es. Propriedades nomeadas s�o identificadas por um nome e um identificador global exclusivo (GUID) para um conjunto de propriedades. O nome pode ser um n�mero ou uma cadeia de caracteres. Para Microsoft Outlook 2013 ou Microsoft Outlook 2010, o conjunto de propriedades � geralmente um namespace definido por Outlook�2013 ou Outlook�2010, como **PSETID_Appointment**.</span><span class="sxs-lookup"><span data-stu-id="dbd5a-p101">MAPI provides a facility for assigning names to certain properties, for mapping these names to unique identifiers, and for making this name-to-identifier mapping persistent across sessions. Named properties are identified by a name and a globally unique identifier (GUID) for a property set. The name can be a number or a string. For Microsoft Outlook 2013 or Microsoft Outlook 2010, the property set is often a namespace defined by Outlook 2013 or Outlook 2010, such as **PSETID_Appointment**.</span></span> 
  
<span data-ttu-id="dbd5a-p102">Named properties are manipulated by using the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) function and the [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) function. The name and the property set GUID are passed to the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) function to obtain a property identifier that is valid for the current MAPI session. Because this property identifier can vary from computer to computer, the only consistent way to access a named property is to know its name and property set GUID. The range for identifiers is always in the 0x8000 and 0xFFFE range.</span><span class="sxs-lookup"><span data-stu-id="dbd5a-p102">Named properties are manipulated by using the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) function and the [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) function. The name and the property set GUID are passed to the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) function to obtain a property identifier that is valid for the current MAPI session. Because this property identifier can vary from computer to computer, the only consistent way to access a named property is to know its name and property set GUID. The range for identifiers is always in the 0x8000 and 0xFFFE range.</span></span> 
  
<span data-ttu-id="dbd5a-p103">Any object that implements the [IMAPIProp: IUnknown](imapipropiunknown.md) interface can support named properties. Specifically, a MAPI service provider or a MAPI client must implement [IMAPIProp::GetProps](imapiprop-getprops.md) to get values of named properties. Setting named properties used by Outlook�2013 or Outlook�2010 is not supported because of the risk of corrupting data that is shared with other MAPI providers or clients.</span><span class="sxs-lookup"><span data-stu-id="dbd5a-p103">Any object that implements the [IMAPIProp : IUnknown](imapipropiunknown.md) interface can support named properties. Specifically, a MAPI service provider or a MAPI client must implement [IMAPIProp::GetProps](imapiprop-getprops.md) to get values of named properties. Setting named properties used by Outlook 2013 or Outlook 2010 is not supported because of the risk of corrupting data that is shared with other MAPI providers or clients.</span></span> 
  
<span data-ttu-id="dbd5a-p104">Outlook�2013 and Outlook�2010 use MAPI named properties to implement many of their features, for example, attachment security and meeting counter-proposals. Above this underlying data, Outlook�2013 and Outlook�2010 expose some of these properties as item properties in their Outlook�2013 and Outlook�2010 object models. For example, the **Email1Address** property of the **ContactItem** object in the object model corresponds to the named [Propriedade can�nico de PidLidEmail1EmailAddress](pidlidemail1emailaddress-canonical-property.md) in the **PSETID_Address** namespace. But in general, due to concerns for compatibility and data integrity, many of the MAPI properties that are used by Outlook�2013 and Outlook�2010 are not exposed in the object model.</span><span class="sxs-lookup"><span data-stu-id="dbd5a-p104">Outlook 2013 and Outlook 2010 use MAPI named properties to implement many of their features, for example, attachment security and meeting counter-proposals. Above this underlying data, Outlook 2013 and Outlook 2010 expose some of these properties as item properties in their Outlook 2013 and Outlook 2010 object models. For example, the **Email1Address** property of the **ContactItem** object in the object model corresponds to the named [PidLidEmail1EmailAddress Canonical Property](pidlidemail1emailaddress-canonical-property.md) in the **PSETID_Address** namespace. But in general, due to concerns for compatibility and data integrity, many of the MAPI properties that are used by Outlook 2013 and Outlook 2010 are not exposed in the object model.</span></span> 
  
<span data-ttu-id="dbd5a-120">Esta refer�ncia descreve um n�mero de propriedades nomeadas listadas abaixo.</span><span class="sxs-lookup"><span data-stu-id="dbd5a-120">This reference describes a number of named properties that are listed below.</span></span>
  
<span data-ttu-id="dbd5a-121">Propriedades nomeadas no namespace **PSETID_Address** s�o as seguintes:</span><span class="sxs-lookup"><span data-stu-id="dbd5a-121">Named properties in the **PSETID_Address** namespace are the following:</span></span> 
  
- [<span data-ttu-id="dbd5a-122">Propriedade can�nico de PidLidEmail1AddressType</span><span class="sxs-lookup"><span data-stu-id="dbd5a-122">PidLidEmail1AddressType Canonical Property</span></span>](pidlidemail1addresstype-canonical-property.md)
    
- [<span data-ttu-id="dbd5a-123">Propriedade can�nico de PidLidEmail1EmailAddress</span><span class="sxs-lookup"><span data-stu-id="dbd5a-123">PidLidEmail1EmailAddress Canonical Property</span></span>](pidlidemail1emailaddress-canonical-property.md)
    
- [<span data-ttu-id="dbd5a-124">Propriedade can�nico de PidLidEmail1OriginalEntryId</span><span class="sxs-lookup"><span data-stu-id="dbd5a-124">PidLidEmail1OriginalEntryId Canonical Property</span></span>](pidlidemail1originalentryid-canonical-property.md)
    
- [<span data-ttu-id="dbd5a-125">Propriedade can�nico de PidLidEmail2AddressType</span><span class="sxs-lookup"><span data-stu-id="dbd5a-125">PidLidEmail2AddressType Canonical Property</span></span>](pidlidemail2addresstype-canonical-property.md)
    
- [<span data-ttu-id="dbd5a-126">Propriedade can�nico de PidLidEmail2DisplayName</span><span class="sxs-lookup"><span data-stu-id="dbd5a-126">PidLidEmail2DisplayName Canonical Property</span></span>](pidlidemail2displayname-canonical-property.md)
    
- [<span data-ttu-id="dbd5a-127">Propriedade can�nico de PidLidEmail2EmailAddress</span><span class="sxs-lookup"><span data-stu-id="dbd5a-127">PidLidEmail2EmailAddress Canonical Property</span></span>](pidlidemail2emailaddress-canonical-property.md)
    
- [<span data-ttu-id="dbd5a-128">Propriedade can�nico de PidLidEmail2OriginalDisplayName</span><span class="sxs-lookup"><span data-stu-id="dbd5a-128">PidLidEmail2OriginalDisplayName Canonical Property</span></span>](pidlidemail2originaldisplayname-canonical-property.md)
    
- [<span data-ttu-id="dbd5a-129">Propriedade can�nico de PidLidEmail2OriginalEntryId</span><span class="sxs-lookup"><span data-stu-id="dbd5a-129">PidLidEmail2OriginalEntryId Canonical Property</span></span>](pidlidemail2originalentryid-canonical-property.md)
    
- [<span data-ttu-id="dbd5a-130">Propriedade can�nico de PidLidEmail3AddressType</span><span class="sxs-lookup"><span data-stu-id="dbd5a-130">PidLidEmail3AddressType Canonical Property</span></span>](pidlidemail3addresstype-canonical-property.md)
    
- [<span data-ttu-id="dbd5a-131">Propriedade can�nico de PidLidEmail3DisplayName</span><span class="sxs-lookup"><span data-stu-id="dbd5a-131">PidLidEmail3DisplayName Canonical Property</span></span>](pidlidemail3displayname-canonical-property.md)
    
- [<span data-ttu-id="dbd5a-132">Propriedade can�nico de PidLidEmail3EmailAddress</span><span class="sxs-lookup"><span data-stu-id="dbd5a-132">PidLidEmail3EmailAddress Canonical Property</span></span>](pidlidemail3emailaddress-canonical-property.md)
    
- [<span data-ttu-id="dbd5a-133">Propriedade can�nico de PidLidEmail3OriginalDisplayName</span><span class="sxs-lookup"><span data-stu-id="dbd5a-133">PidLidEmail3OriginalDisplayName Canonical Property</span></span>](pidlidemail3originaldisplayname-canonical-property.md)
    
- [<span data-ttu-id="dbd5a-134">Propriedade can�nico de PidLidEmail3OriginalEntryId</span><span class="sxs-lookup"><span data-stu-id="dbd5a-134">PidLidEmail3OriginalEntryId Canonical Property</span></span>](pidlidemail3originalentryid-canonical-property.md)
    
- [<span data-ttu-id="dbd5a-135">Propriedade can�nico de PidLidEmail1DisplayName</span><span class="sxs-lookup"><span data-stu-id="dbd5a-135">PidLidEmail1DisplayName Canonical Property</span></span>](pidlidemail1displayname-canonical-property.md)
    
- [<span data-ttu-id="dbd5a-136">Propriedade can�nico de PidLidEmail1OriginalDisplayName</span><span class="sxs-lookup"><span data-stu-id="dbd5a-136">PidLidEmail1OriginalDisplayName Canonical Property</span></span>](pidlidemail1originaldisplayname-canonical-property.md)
    
- [<span data-ttu-id="dbd5a-137">Propriedade can�nico de PidLidFileUnder</span><span class="sxs-lookup"><span data-stu-id="dbd5a-137">PidLidFileUnder Canonical Property</span></span>](pidlidfileunder-canonical-property.md)
    
- [<span data-ttu-id="dbd5a-138">Propriedade can�nico de PidLidInstantMessagingAddress</span><span class="sxs-lookup"><span data-stu-id="dbd5a-138">PidLidInstantMessagingAddress Canonical Property</span></span>](pidlidinstantmessagingaddress-canonical-property.md)
    
- [<span data-ttu-id="dbd5a-139">Propriedade can�nico de PidLidWorkAddressCity</span><span class="sxs-lookup"><span data-stu-id="dbd5a-139">PidLidWorkAddressCity Canonical Property</span></span>](pidlidworkaddresscity-canonical-property.md)
    
- [<span data-ttu-id="dbd5a-140">Propriedade can�nico de PidLidWorkAddressCountry</span><span class="sxs-lookup"><span data-stu-id="dbd5a-140">PidLidWorkAddressCountry Canonical Property</span></span>](pidlidworkaddresscountry-canonical-property.md)
    
- [<span data-ttu-id="dbd5a-141">Propriedade can�nico de PidLidWorkAddressPostalCode</span><span class="sxs-lookup"><span data-stu-id="dbd5a-141">PidLidWorkAddressPostalCode Canonical Property</span></span>](pidlidworkaddresspostalcode-canonical-property.md)
    
- [<span data-ttu-id="dbd5a-142">Propriedade can�nico de PidLidWorkAddressPostOfficeBox</span><span class="sxs-lookup"><span data-stu-id="dbd5a-142">PidLidWorkAddressPostOfficeBox Canonical Property</span></span>](pidlidworkaddresspostofficebox-canonical-property.md)
    
- [<span data-ttu-id="dbd5a-143">Propriedade can�nico de PidLidWorkAddressState</span><span class="sxs-lookup"><span data-stu-id="dbd5a-143">PidLidWorkAddressState Canonical Property</span></span>](pidlidworkaddressstate-canonical-property.md)
    
- [<span data-ttu-id="dbd5a-144">Propriedade can�nico de PidLidWorkAddressStreet</span><span class="sxs-lookup"><span data-stu-id="dbd5a-144">PidLidWorkAddressStreet Canonical Property</span></span>](pidlidworkaddressstreet-canonical-property.md)
    
- [<span data-ttu-id="dbd5a-145">Propriedade can�nico de PidLidYomiCompanyName</span><span class="sxs-lookup"><span data-stu-id="dbd5a-145">PidLidYomiCompanyName Canonical Property</span></span>](pidlidyomicompanyname-canonical-property.md)
    
- [<span data-ttu-id="dbd5a-146">Propriedade can�nico de PidLidYomiFirstName</span><span class="sxs-lookup"><span data-stu-id="dbd5a-146">PidLidYomiFirstName Canonical Property</span></span>](pidlidyomifirstname-canonical-property.md)
    
- [<span data-ttu-id="dbd5a-147">Propriedade can�nico de PidLidYomiLastName</span><span class="sxs-lookup"><span data-stu-id="dbd5a-147">PidLidYomiLastName Canonical Property</span></span>](pidlidyomilastname-canonical-property.md)
    
<span data-ttu-id="dbd5a-148">Propriedades nomeadas no namespace **PSETID_Appointment** s�o as seguintes:</span><span class="sxs-lookup"><span data-stu-id="dbd5a-148">Named properties in the **PSETID_Appointment** namespace are the following:</span></span> 
  
- [<span data-ttu-id="dbd5a-149">Propriedade can�nico de PidLidAllAttendeesString</span><span class="sxs-lookup"><span data-stu-id="dbd5a-149">PidLidAllAttendeesString Canonical Property</span></span>](pidlidallattendeesstring-canonical-property.md)
    
- [<span data-ttu-id="dbd5a-150">Propriedade can�nico de PidLidAppointmentCounterProposal</span><span class="sxs-lookup"><span data-stu-id="dbd5a-150">PidLidAppointmentCounterProposal Canonical Property</span></span>](pidlidappointmentcounterproposal-canonical-property.md)
    
- [<span data-ttu-id="dbd5a-151">Propriedade can�nico de PidLidAppointmentDuration</span><span class="sxs-lookup"><span data-stu-id="dbd5a-151">PidLidAppointmentDuration Canonical Property</span></span>](pidlidappointmentduration-canonical-property.md)
    
- [<span data-ttu-id="dbd5a-152">Propriedade can�nico de PidLidAppointmentEndWhole</span><span class="sxs-lookup"><span data-stu-id="dbd5a-152">PidLidAppointmentEndWhole Canonical Property</span></span>](pidlidappointmentendwhole-canonical-property.md)
    
- [<span data-ttu-id="dbd5a-153">Propriedade can�nico de PidLidAppointmentStartWhole</span><span class="sxs-lookup"><span data-stu-id="dbd5a-153">PidLidAppointmentStartWhole Canonical Property</span></span>](pidlidappointmentstartwhole-canonical-property.md)
    
- [<span data-ttu-id="dbd5a-154">Propriedade can�nico de PidLidBusyStatus</span><span class="sxs-lookup"><span data-stu-id="dbd5a-154">PidLidBusyStatus Canonical Property</span></span>](pidlidbusystatus-canonical-property.md)
    
- [<span data-ttu-id="dbd5a-155">Propriedade can�nico de PidLidCcAttendeesString</span><span class="sxs-lookup"><span data-stu-id="dbd5a-155">PidLidCcAttendeesString Canonical Property</span></span>](pidlidccattendeesstring-canonical-property.md)
    
- [<span data-ttu-id="dbd5a-156">Propriedade can�nico de PidLidLocation</span><span class="sxs-lookup"><span data-stu-id="dbd5a-156">PidLidLocation Canonical Property</span></span>](pidlidlocation-canonical-property.md)
    
- [<span data-ttu-id="dbd5a-157">Propriedade can�nico de PidLidRecurring</span><span class="sxs-lookup"><span data-stu-id="dbd5a-157">PidLidRecurring Canonical Property</span></span>](pidlidrecurring-canonical-property.md)
    
- [<span data-ttu-id="dbd5a-158">Propriedade can�nico de PidLidToAttendeesString</span><span class="sxs-lookup"><span data-stu-id="dbd5a-158">PidLidToAttendeesString Canonical Property</span></span>](pidlidtoattendeesstring-canonical-property.md)
    
<span data-ttu-id="dbd5a-159">Propriedades nomeadas no namespace **PSETID_Common** s�o as seguintes:</span><span class="sxs-lookup"><span data-stu-id="dbd5a-159">Named properties in the **PSETID_Common** namespace are the following:</span></span> 
  
- [<span data-ttu-id="dbd5a-160">Propriedade can�nico de PidLidCommonEnd</span><span class="sxs-lookup"><span data-stu-id="dbd5a-160">PidLidCommonEnd Canonical Property</span></span>](pidlidcommonend-canonical-property.md)
    
- [<span data-ttu-id="dbd5a-161">Propriedade can�nico de PidLidCommonStart</span><span class="sxs-lookup"><span data-stu-id="dbd5a-161">PidLidCommonStart Canonical Property</span></span>](pidlidcommonstart-canonical-property.md)
    
- [<span data-ttu-id="dbd5a-162">Propriedade can�nico de PidLidCompanies</span><span class="sxs-lookup"><span data-stu-id="dbd5a-162">PidLidCompanies Canonical Property</span></span>](pidlidcompanies-canonical-property.md)
    
- [<span data-ttu-id="dbd5a-163">Propriedade can�nico de PidLidContacts</span><span class="sxs-lookup"><span data-stu-id="dbd5a-163">PidLidContacts Canonical Property</span></span>](pidlidcontacts-canonical-property.md)
    
- [<span data-ttu-id="dbd5a-164">Propriedade can�nico de PidLidCustomFlag</span><span class="sxs-lookup"><span data-stu-id="dbd5a-164">PidLidCustomFlag Canonical Property</span></span>](pidlidcustomflag-canonical-property.md)
    
- [<span data-ttu-id="dbd5a-165">Propriedade can�nico de PidLidFormPropStream</span><span class="sxs-lookup"><span data-stu-id="dbd5a-165">PidLidFormPropStream Canonical Property</span></span>](pidlidformpropstream-canonical-property.md)
    
- [<span data-ttu-id="dbd5a-166">Propriedade can�nico de PidLidFormStorage</span><span class="sxs-lookup"><span data-stu-id="dbd5a-166">PidLidFormStorage Canonical Property</span></span>](pidlidformstorage-canonical-property.md)
    
- [<span data-ttu-id="dbd5a-167">Propriedade can�nico de PidLidHeaderItem</span><span class="sxs-lookup"><span data-stu-id="dbd5a-167">PidLidHeaderItem Canonical Property</span></span>](pidlidheaderitem-canonical-property.md)
    
- [<span data-ttu-id="dbd5a-168">Propriedade can�nico de PidLidPageDirStream</span><span class="sxs-lookup"><span data-stu-id="dbd5a-168">PidLidPageDirStream Canonical Property</span></span>](pidlidpagedirstream-canonical-property.md)
    
- [<span data-ttu-id="dbd5a-169">Propriedade can�nico de PidLidPropertyDefinitionStream</span><span class="sxs-lookup"><span data-stu-id="dbd5a-169">PidLidPropertyDefinitionStream Canonical Property</span></span>](pidlidpropertydefinitionstream-canonical-property.md)
    
- [<span data-ttu-id="dbd5a-170">Propriedade can�nico de PidLidReminderSet</span><span class="sxs-lookup"><span data-stu-id="dbd5a-170">PidLidReminderSet Canonical Property</span></span>](pidlidreminderset-canonical-property.md)
    
- [<span data-ttu-id="dbd5a-171">Propriedade can�nico de PidLidReminderTime</span><span class="sxs-lookup"><span data-stu-id="dbd5a-171">PidLidReminderTime Canonical Property</span></span>](pidlidremindertime-canonical-property.md)
    
- [<span data-ttu-id="dbd5a-172">Propriedade can�nico de PidLidFlagRequest</span><span class="sxs-lookup"><span data-stu-id="dbd5a-172">PidLidFlagRequest Canonical Property</span></span>](pidlidflagrequest-canonical-property.md)
    
- [<span data-ttu-id="dbd5a-173">Propriedade can�nico de PidLidScriptStream</span><span class="sxs-lookup"><span data-stu-id="dbd5a-173">PidLidScriptStream Canonical Property</span></span>](pidlidscriptstream-canonical-property.md)
    
- [<span data-ttu-id="dbd5a-174">Propriedade can�nico de PidLidSmartNoAttach</span><span class="sxs-lookup"><span data-stu-id="dbd5a-174">PidLidSmartNoAttach Canonical Property</span></span>](pidlidsmartnoattach-canonical-property.md)
    
- [<span data-ttu-id="dbd5a-175">Propriedade can�nico de PidLidToDoTitle</span><span class="sxs-lookup"><span data-stu-id="dbd5a-175">PidLidToDoTitle Canonical Property</span></span>](pidlidtodotitle-canonical-property.md)
    
- [<span data-ttu-id="dbd5a-176">Propriedade can�nico de PidLidUseTnef</span><span class="sxs-lookup"><span data-stu-id="dbd5a-176">PidLidUseTnef Canonical Property</span></span>](pidlidusetnef-canonical-property.md)
    
<span data-ttu-id="dbd5a-177">Propriedades nomeadas no namespace **PSETID_Meeting** s�o as seguintes:</span><span class="sxs-lookup"><span data-stu-id="dbd5a-177">Named properties in the **PSETID_Meeting** namespace are the following:</span></span> 
  
- [<span data-ttu-id="dbd5a-178">Propriedade can�nico de PidLidMeetingType</span><span class="sxs-lookup"><span data-stu-id="dbd5a-178">PidLidMeetingType Canonical Property</span></span>](pidlidmeetingtype-canonical-property.md)
    
<span data-ttu-id="dbd5a-179">Propriedades nomeadas no namespace **PSETID_Task** s�o as seguintes:</span><span class="sxs-lookup"><span data-stu-id="dbd5a-179">Named properties in the **PSETID_Task** namespace are the following:</span></span> 
  
- [<span data-ttu-id="dbd5a-180">Propriedade can�nico de PidLidTaskActualEffort</span><span class="sxs-lookup"><span data-stu-id="dbd5a-180">PidLidTaskActualEffort Canonical Property</span></span>](pidlidtaskactualeffort-canonical-property.md)
    
- [<span data-ttu-id="dbd5a-181">Propriedade can�nico de PidLidTaskDueDate</span><span class="sxs-lookup"><span data-stu-id="dbd5a-181">PidLidTaskDueDate Canonical Property</span></span>](pidlidtaskduedate-canonical-property.md)
    
- [<span data-ttu-id="dbd5a-182">Propriedade can�nico de PidLidTaskEstimatedEffort</span><span class="sxs-lookup"><span data-stu-id="dbd5a-182">PidLidTaskEstimatedEffort Canonical Property</span></span>](pidlidtaskestimatedeffort-canonical-property.md)
    
- [<span data-ttu-id="dbd5a-183">Propriedade can�nico de PidLidTaskFRecurring</span><span class="sxs-lookup"><span data-stu-id="dbd5a-183">PidLidTaskFRecurring Canonical Property</span></span>](pidlidtaskfrecurring-canonical-property.md)
    
- [<span data-ttu-id="dbd5a-184">Propriedade can�nico de PidLidTaskStartDate</span><span class="sxs-lookup"><span data-stu-id="dbd5a-184">PidLidTaskStartDate Canonical Property</span></span>](pidlidtaskstartdate-canonical-property.md)
    
- [<span data-ttu-id="dbd5a-185">Propriedade can�nico de PidLidTaskStatus</span><span class="sxs-lookup"><span data-stu-id="dbd5a-185">PidLidTaskStatus Canonical Property</span></span>](pidlidtaskstatus-canonical-property.md)
    
<span data-ttu-id="dbd5a-186">Propriedades nomeadas no namespace **PS_INTERNET_HEADERS** s�o as seguintes:</span><span class="sxs-lookup"><span data-stu-id="dbd5a-186">Named properties in the **PS_INTERNET_HEADERS** namespace are the following:</span></span> 
  
- [<span data-ttu-id="dbd5a-187">Propriedade can�nico de PidTagInternetReturnPath</span><span class="sxs-lookup"><span data-stu-id="dbd5a-187">PidTagInternetReturnPath Canonical Property</span></span>](pidtaginternetreturnpath-canonical-property.md)
    
<span data-ttu-id="dbd5a-188">Propriedades nomeadas no namespace **PSETID_Log** s�o as seguintes:</span><span class="sxs-lookup"><span data-stu-id="dbd5a-188">Named properties in the **PSETID_Log** namespace are the following:</span></span> 
  
- [<span data-ttu-id="dbd5a-189">Propriedade can�nico de PidLidLogDuration</span><span class="sxs-lookup"><span data-stu-id="dbd5a-189">PidLidLogDuration Canonical Property</span></span>](pidlidlogduration-canonical-property.md)
    
- [<span data-ttu-id="dbd5a-190">Propriedade can�nico de PidLidLogEnd</span><span class="sxs-lookup"><span data-stu-id="dbd5a-190">PidLidLogEnd Canonical Property</span></span>](pidlidlogend-canonical-property.md)
    
- [<span data-ttu-id="dbd5a-191">Propriedade can�nico de PidLidLogStart</span><span class="sxs-lookup"><span data-stu-id="dbd5a-191">PidLidLogStart Canonical Property</span></span>](pidlidlogstart-canonical-property.md)
    
- [<span data-ttu-id="dbd5a-192">Propriedade can�nico de PidLidLogType</span><span class="sxs-lookup"><span data-stu-id="dbd5a-192">PidLidLogType Canonical Property</span></span>](pidlidlogtype-canonical-property.md)
    
<span data-ttu-id="dbd5a-193">Propriedades nomeadas no namespace **PS_PUBLIC_STRINGS** s�o as seguintes:</span><span class="sxs-lookup"><span data-stu-id="dbd5a-193">Named properties in the **PS_PUBLIC_STRINGS** namespace are the following:</span></span> 
  
- [<span data-ttu-id="dbd5a-194">Propriedade can�nico de PidNameKeywords</span><span class="sxs-lookup"><span data-stu-id="dbd5a-194">PidNameKeywords Canonical Property</span></span>](pidnamekeywords-canonical-property.md)
    
- [<span data-ttu-id="dbd5a-195">Propriedade can�nico de PidNameExchangeJunkEmailMoveStamp</span><span class="sxs-lookup"><span data-stu-id="dbd5a-195">PidNameExchangeJunkEmailMoveStamp Canonical Property</span></span>](pidnameexchangejunkemailmovestamp-canonical-property.md)
    
## <a name="see-also"></a><span data-ttu-id="dbd5a-196">Ver tamb�m</span><span class="sxs-lookup"><span data-stu-id="dbd5a-196">See also</span></span>



[<span data-ttu-id="dbd5a-197">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="dbd5a-197">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="dbd5a-198">Determinar se o Outlook baixou somente o cabeçalho de uma mensagem</span><span class="sxs-lookup"><span data-stu-id="dbd5a-198">Determine if Outlook Downloaded Only the Header of a Message</span></span>](how-to-determine-if-outlook-downloaded-only-the-header-of-a-message.md)
  
[<span data-ttu-id="dbd5a-199">Obter o endereço de Email de um item de contato</span><span class="sxs-lookup"><span data-stu-id="dbd5a-199">Get the Email Address of a Contact Item</span></span>](how-to-get-the-email-address-of-a-contact-item.md)
  
[<span data-ttu-id="dbd5a-200">Remover a definição de formulário personalizada salva com uma mensagem</span><span class="sxs-lookup"><span data-stu-id="dbd5a-200">Remove Custom Form Definition Saved With a Message</span></span>](how-to-remove-custom-form-definition-saved-with-a-message.md)

