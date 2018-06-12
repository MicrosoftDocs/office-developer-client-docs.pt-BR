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
# <a name="about-named-properties-used-by-outlook"></a>Sobre propriedades nomeadas usadas pelo Outlook

  
  
**Aplica-se a**: Outlook 
  
MAPI fornece uma facilidade para atribuir nomes para determinadas propriedades para mapear esses nomes para identificadores exclusivos e para tornar os esse nome-para-identificador mapeamento persistente entre sess�es. Propriedades nomeadas s�o identificadas por um nome e um identificador global exclusivo (GUID) para um conjunto de propriedades. O nome pode ser um n�mero ou uma cadeia de caracteres. Para Microsoft Outlook 2013 ou Microsoft Outlook 2010, o conjunto de propriedades � geralmente um namespace definido por Outlook�2013 ou Outlook�2010, como **PSETID_Appointment**. 
  
Named properties are manipulated by using the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) function and the [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) function. The name and the property set GUID are passed to the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) function to obtain a property identifier that is valid for the current MAPI session. Because this property identifier can vary from computer to computer, the only consistent way to access a named property is to know its name and property set GUID. The range for identifiers is always in the 0x8000 and 0xFFFE range. 
  
Any object that implements the [IMAPIProp: IUnknown](imapipropiunknown.md) interface can support named properties. Specifically, a MAPI service provider or a MAPI client must implement [IMAPIProp::GetProps](imapiprop-getprops.md) to get values of named properties. Setting named properties used by Outlook�2013 or Outlook�2010 is not supported because of the risk of corrupting data that is shared with other MAPI providers or clients. 
  
Outlook�2013 and Outlook�2010 use MAPI named properties to implement many of their features, for example, attachment security and meeting counter-proposals. Above this underlying data, Outlook�2013 and Outlook�2010 expose some of these properties as item properties in their Outlook�2013 and Outlook�2010 object models. For example, the **Email1Address** property of the **ContactItem** object in the object model corresponds to the named [Propriedade can�nico de PidLidEmail1EmailAddress](pidlidemail1emailaddress-canonical-property.md) in the **PSETID_Address** namespace. But in general, due to concerns for compatibility and data integrity, many of the MAPI properties that are used by Outlook�2013 and Outlook�2010 are not exposed in the object model. 
  
Esta refer�ncia descreve um n�mero de propriedades nomeadas listadas abaixo.
  
Propriedades nomeadas no namespace **PSETID_Address** s�o as seguintes: 
  
- [Propriedade can�nico de PidLidEmail1AddressType](pidlidemail1addresstype-canonical-property.md)
    
- [Propriedade can�nico de PidLidEmail1EmailAddress](pidlidemail1emailaddress-canonical-property.md)
    
- [Propriedade can�nico de PidLidEmail1OriginalEntryId](pidlidemail1originalentryid-canonical-property.md)
    
- [Propriedade can�nico de PidLidEmail2AddressType](pidlidemail2addresstype-canonical-property.md)
    
- [Propriedade can�nico de PidLidEmail2DisplayName](pidlidemail2displayname-canonical-property.md)
    
- [Propriedade can�nico de PidLidEmail2EmailAddress](pidlidemail2emailaddress-canonical-property.md)
    
- [Propriedade can�nico de PidLidEmail2OriginalDisplayName](pidlidemail2originaldisplayname-canonical-property.md)
    
- [Propriedade can�nico de PidLidEmail2OriginalEntryId](pidlidemail2originalentryid-canonical-property.md)
    
- [Propriedade can�nico de PidLidEmail3AddressType](pidlidemail3addresstype-canonical-property.md)
    
- [Propriedade can�nico de PidLidEmail3DisplayName](pidlidemail3displayname-canonical-property.md)
    
- [Propriedade can�nico de PidLidEmail3EmailAddress](pidlidemail3emailaddress-canonical-property.md)
    
- [Propriedade can�nico de PidLidEmail3OriginalDisplayName](pidlidemail3originaldisplayname-canonical-property.md)
    
- [Propriedade can�nico de PidLidEmail3OriginalEntryId](pidlidemail3originalentryid-canonical-property.md)
    
- [Propriedade can�nico de PidLidEmail1DisplayName](pidlidemail1displayname-canonical-property.md)
    
- [Propriedade can�nico de PidLidEmail1OriginalDisplayName](pidlidemail1originaldisplayname-canonical-property.md)
    
- [Propriedade can�nico de PidLidFileUnder](pidlidfileunder-canonical-property.md)
    
- [Propriedade can�nico de PidLidInstantMessagingAddress](pidlidinstantmessagingaddress-canonical-property.md)
    
- [Propriedade can�nico de PidLidWorkAddressCity](pidlidworkaddresscity-canonical-property.md)
    
- [Propriedade can�nico de PidLidWorkAddressCountry](pidlidworkaddresscountry-canonical-property.md)
    
- [Propriedade can�nico de PidLidWorkAddressPostalCode](pidlidworkaddresspostalcode-canonical-property.md)
    
- [Propriedade can�nico de PidLidWorkAddressPostOfficeBox](pidlidworkaddresspostofficebox-canonical-property.md)
    
- [Propriedade can�nico de PidLidWorkAddressState](pidlidworkaddressstate-canonical-property.md)
    
- [Propriedade can�nico de PidLidWorkAddressStreet](pidlidworkaddressstreet-canonical-property.md)
    
- [Propriedade can�nico de PidLidYomiCompanyName](pidlidyomicompanyname-canonical-property.md)
    
- [Propriedade can�nico de PidLidYomiFirstName](pidlidyomifirstname-canonical-property.md)
    
- [Propriedade can�nico de PidLidYomiLastName](pidlidyomilastname-canonical-property.md)
    
Propriedades nomeadas no namespace **PSETID_Appointment** s�o as seguintes: 
  
- [Propriedade can�nico de PidLidAllAttendeesString](pidlidallattendeesstring-canonical-property.md)
    
- [Propriedade can�nico de PidLidAppointmentCounterProposal](pidlidappointmentcounterproposal-canonical-property.md)
    
- [Propriedade can�nico de PidLidAppointmentDuration](pidlidappointmentduration-canonical-property.md)
    
- [Propriedade can�nico de PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)
    
- [Propriedade can�nico de PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)
    
- [Propriedade can�nico de PidLidBusyStatus](pidlidbusystatus-canonical-property.md)
    
- [Propriedade can�nico de PidLidCcAttendeesString](pidlidccattendeesstring-canonical-property.md)
    
- [Propriedade can�nico de PidLidLocation](pidlidlocation-canonical-property.md)
    
- [Propriedade can�nico de PidLidRecurring](pidlidrecurring-canonical-property.md)
    
- [Propriedade can�nico de PidLidToAttendeesString](pidlidtoattendeesstring-canonical-property.md)
    
Propriedades nomeadas no namespace **PSETID_Common** s�o as seguintes: 
  
- [Propriedade can�nico de PidLidCommonEnd](pidlidcommonend-canonical-property.md)
    
- [Propriedade can�nico de PidLidCommonStart](pidlidcommonstart-canonical-property.md)
    
- [Propriedade can�nico de PidLidCompanies](pidlidcompanies-canonical-property.md)
    
- [Propriedade can�nico de PidLidContacts](pidlidcontacts-canonical-property.md)
    
- [Propriedade can�nico de PidLidCustomFlag](pidlidcustomflag-canonical-property.md)
    
- [Propriedade can�nico de PidLidFormPropStream](pidlidformpropstream-canonical-property.md)
    
- [Propriedade can�nico de PidLidFormStorage](pidlidformstorage-canonical-property.md)
    
- [Propriedade can�nico de PidLidHeaderItem](pidlidheaderitem-canonical-property.md)
    
- [Propriedade can�nico de PidLidPageDirStream](pidlidpagedirstream-canonical-property.md)
    
- [Propriedade can�nico de PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md)
    
- [Propriedade can�nico de PidLidReminderSet](pidlidreminderset-canonical-property.md)
    
- [Propriedade can�nico de PidLidReminderTime](pidlidremindertime-canonical-property.md)
    
- [Propriedade can�nico de PidLidFlagRequest](pidlidflagrequest-canonical-property.md)
    
- [Propriedade can�nico de PidLidScriptStream](pidlidscriptstream-canonical-property.md)
    
- [Propriedade can�nico de PidLidSmartNoAttach](pidlidsmartnoattach-canonical-property.md)
    
- [Propriedade can�nico de PidLidToDoTitle](pidlidtodotitle-canonical-property.md)
    
- [Propriedade can�nico de PidLidUseTnef](pidlidusetnef-canonical-property.md)
    
Propriedades nomeadas no namespace **PSETID_Meeting** s�o as seguintes: 
  
- [Propriedade can�nico de PidLidMeetingType](pidlidmeetingtype-canonical-property.md)
    
Propriedades nomeadas no namespace **PSETID_Task** s�o as seguintes: 
  
- [Propriedade can�nico de PidLidTaskActualEffort](pidlidtaskactualeffort-canonical-property.md)
    
- [Propriedade can�nico de PidLidTaskDueDate](pidlidtaskduedate-canonical-property.md)
    
- [Propriedade can�nico de PidLidTaskEstimatedEffort](pidlidtaskestimatedeffort-canonical-property.md)
    
- [Propriedade can�nico de PidLidTaskFRecurring](pidlidtaskfrecurring-canonical-property.md)
    
- [Propriedade can�nico de PidLidTaskStartDate](pidlidtaskstartdate-canonical-property.md)
    
- [Propriedade can�nico de PidLidTaskStatus](pidlidtaskstatus-canonical-property.md)
    
Propriedades nomeadas no namespace **PS_INTERNET_HEADERS** s�o as seguintes: 
  
- [Propriedade can�nico de PidTagInternetReturnPath](pidtaginternetreturnpath-canonical-property.md)
    
Propriedades nomeadas no namespace **PSETID_Log** s�o as seguintes: 
  
- [Propriedade can�nico de PidLidLogDuration](pidlidlogduration-canonical-property.md)
    
- [Propriedade can�nico de PidLidLogEnd](pidlidlogend-canonical-property.md)
    
- [Propriedade can�nico de PidLidLogStart](pidlidlogstart-canonical-property.md)
    
- [Propriedade can�nico de PidLidLogType](pidlidlogtype-canonical-property.md)
    
Propriedades nomeadas no namespace **PS_PUBLIC_STRINGS** s�o as seguintes: 
  
- [Propriedade can�nico de PidNameKeywords](pidnamekeywords-canonical-property.md)
    
- [Propriedade can�nico de PidNameExchangeJunkEmailMoveStamp](pidnameexchangejunkemailmovestamp-canonical-property.md)
    
## <a name="see-also"></a>Ver tamb�m



[Constantes MAPI](mapi-constants.md)
  
[Determinar se o Outlook download somente do cabeçalho de uma mensagem](how-to-determine-if-outlook-downloaded-only-the-header-of-a-message.md)
  
[Obter o endereço de Email de um Item de contato](how-to-get-the-email-address-of-a-contact-item.md)
  
[Remova a definição de formulário personalizado salva com uma mensagem](how-to-remove-custom-form-definition-saved-with-a-message.md)

