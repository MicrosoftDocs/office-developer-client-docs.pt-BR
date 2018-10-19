---
title: Sobre as propriedades nomeadas usadas pelo Outlook
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 8c245ec2-bb18-ecf0-b4ad-8c164c5924cf
description: 'Última modificação: 25 de julho de 2012'
ms.openlocfilehash: aa4d52d25f120e8b3e2a4c0dcaa4845ad576127a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566226"
---
# <a name="about-named-properties-used-by-outlook"></a>Sobre as propriedades nomeadas usadas pelo Outlook

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O MAPI fornece um recurso para atribuir nomes a certas propriedades, para mapear esses nomes para identificadores exclusivos e para fazer esse mapeamento nome-para-identificador persistente nas sessões. As propriedades nomeadas são identificadas por um nome e um identificador global exclusivo (GUID) para um conjunto de propriedades. O nome pode ser um número ou uma cadeia de caracteres. No Microsoft Outlook 2013 ou no Microsoft Outlook 2010, o conjunto de propriedades geralmente é um namespace definido pelo Outlook 2013 ou 2010, como **PSETID_Appointment**. 
  
Propriedades nomeadas são manipuladas usando a função [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) e a função [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md). O nome e o GUID do conjunto de propriedades são passados para a função [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) para obter um identificador de propriedade que seja válido para a sessão MAPI atual. Como esse identificador de propriedade pode variar entre computadores, a única maneira consistente de acessar uma propriedade nomeada é saber seu nome e GUID do conjunto de propriedades. O intervalo de identificadores está sempre entre 0x8000 e 0xFFFE. 
  
Qualquer objeto que implementa a interface [IMAPIProp: IUnknown](imapipropiunknown.md) pode suportar propriedades nomeadas. Especificamente, um provedor de serviços MAPI ou um cliente MAPI precisa implementar [IMAPIProp::GetProps](imapiprop-getprops.md) para obter valores de propriedades nomeadas. A configuração de propriedades usada pelo Outlook 2013 ou Outlook 2010 não é suportada por causa do risco de corrompimento de dados que é compartilhado com outros provedores ou clientes MAPI. 
  
O Outlook 2013 e o Outlook 2010 usam propriedades nomeadas MAPI para implementar muitos de seus recursos; por exemplo, segurança de anexos e contrapropostas de reuniões. Acima desses dados subjacentes, o Outlook 2013 e o Outlook 2010 expõem algumas dessas propriedades como propriedades de itens em seus modelos de objeto do Outlook 2013 e do Outlook 2010. Por exemplo, a propriedade **Email1Address** do objeto **ContactItem** no modelo de objeto corresponde à nomeada [PidLidEmail1EmailAddress](pidlidemail1emailaddress-canonical-property.md) no namespace **PSETID_Address**. Em geral, porém, em razão de preocupações com compatibilidade e integridade de dados, muitas das propriedades MAPI usadas pelo Outlook 2013 e Outlook 2010 não são expostas no modelo de objeto. 
  
Esta referência descreve diversas propriedades nomeadas que estão listadas abaixo.
  
As propriedades nomeadas no namespace **PSETID_Address** são as seguintes: 
  
- [Propriedade canônica PidLidEmail1AddressType](pidlidemail1addresstype-canonical-property.md)
    
- [Propriedade canônica PidLidEmail1EmailAddress](pidlidemail1emailaddress-canonical-property.md)
    
- [Propriedade canônica PidLidEmail1OriginalEntryId](pidlidemail1originalentryid-canonical-property.md)
    
- [Propriedade canônica PidLidEmail2AddressType](pidlidemail2addresstype-canonical-property.md)
    
- [Propriedade canônica PidLidEmail2DisplayName](pidlidemail2displayname-canonical-property.md)
    
- [Propriedade canônica PidLidEmail2EmailAddress](pidlidemail2emailaddress-canonical-property.md)
    
- [Propriedade canônica PidLidEmail2OriginalDisplayName](pidlidemail2originaldisplayname-canonical-property.md)
    
- [Propriedade canônica PidLidEmail2OriginalEntryId](pidlidemail2originalentryid-canonical-property.md)
    
- [Propriedade canônica PidLidEmail3AddressType](pidlidemail3addresstype-canonical-property.md)
    
- [Propriedade canônica PidLidEmail3DisplayName](pidlidemail3displayname-canonical-property.md)
    
- [Propriedade canônica PidLidEmail3EmailAddress](pidlidemail3emailaddress-canonical-property.md)
    
- [Propriedade canônica PidLidEmail3OriginalDisplayName](pidlidemail3originaldisplayname-canonical-property.md)
    
- [Propriedade canônica PidLidEmail3OriginalEntryId](pidlidemail3originalentryid-canonical-property.md)
    
- [Propriedade canônica PidLidEmail1DisplayName](pidlidemail1displayname-canonical-property.md)
    
- [Propriedade canônica PidLidEmail1OriginalDisplayName](pidlidemail1originaldisplayname-canonical-property.md)
    
- [Propriedade canônica PidLidFileUnder](pidlidfileunder-canonical-property.md)
    
- [Propriedade canônica PidLidInstantMessagingAddress](pidlidinstantmessagingaddress-canonical-property.md)
    
- [Propriedade canônica PidLidWorkAddressCity](pidlidworkaddresscity-canonical-property.md)
    
- [Propriedade canônica PidLidWorkAddressCountry](pidlidworkaddresscountry-canonical-property.md)
    
- [Propriedade canônica PidLidWorkAddressPostalCode](pidlidworkaddresspostalcode-canonical-property.md)
    
- [Propriedade canônica PidLidWorkAddressPostOfficeBox](pidlidworkaddresspostofficebox-canonical-property.md)
    
- [Propriedade canônica PidLidWorkAddressState](pidlidworkaddressstate-canonical-property.md)
    
- [Propriedade canônica PidLidWorkAddressStreet](pidlidworkaddressstreet-canonical-property.md)
    
- [Propriedade canônica PidLidYomiCompanyName](pidlidyomicompanyname-canonical-property.md)
    
- [Propriedade canônica PidLidYomiFirstName](pidlidyomifirstname-canonical-property.md)
    
- [Propriedade canônica PidLidYomiLastName](pidlidyomilastname-canonical-property.md)
    
As propriedades nomeadas no namespace **PSETID_Appointment** são as seguintes: 
  
- [Propriedade canônica PidLidAllAttendeesString](pidlidallattendeesstring-canonical-property.md)
    
- [Propriedade canônica PidLidAppointmentCounterProposal](pidlidappointmentcounterproposal-canonical-property.md)
    
- [Propriedade canônica PidLidAppointmentDuration](pidlidappointmentduration-canonical-property.md)
    
- [Propriedade canônica PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)
    
- [Propriedade canônica PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)
    
- [Propriedade canônica PidLidBusyStatus](pidlidbusystatus-canonical-property.md)
    
- [Propriedade canônica PidLidCcAttendeesString](pidlidccattendeesstring-canonical-property.md)
    
- [Propriedade canônica PidLidLocation](pidlidlocation-canonical-property.md)
    
- [Propriedade canônica PidLidRecurring](pidlidrecurring-canonical-property.md)
    
- [Propriedade canônica PidLidToAttendeesString](pidlidtoattendeesstring-canonical-property.md)
    
As propriedades nomeadas no namespace **PSETID_Common** são as seguintes: 
  
- [Propriedade canônica PidLidCommonEnd](pidlidcommonend-canonical-property.md)
    
- [Propriedade canônica PidLidCommonStart](pidlidcommonstart-canonical-property.md)
    
- [Propriedade canônica PidLidCompanies](pidlidcompanies-canonical-property.md)
    
- [Propriedade canônica PidLidContacts](pidlidcontacts-canonical-property.md)
    
- [Propriedade canônica PidLidCustomFlag](pidlidcustomflag-canonical-property.md)
    
- [Propriedade canônica PidLidFormPropStream](pidlidformpropstream-canonical-property.md)
    
- [Propriedade canônica PidLidFormStorage](pidlidformstorage-canonical-property.md)
    
- [Propriedade canônica PidLidHeaderItem](pidlidheaderitem-canonical-property.md)
    
- [Propriedade canônica PidLidPageDirStream](pidlidpagedirstream-canonical-property.md)
    
- [Propriedade canônica PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md)
    
- [Propriedade canônica PidLidReminderSet](pidlidreminderset-canonical-property.md)
    
- [Propriedade canônica PidLidReminderTime](pidlidremindertime-canonical-property.md)
    
- [Propriedade canônica PidLidFlagRequest](pidlidflagrequest-canonical-property.md)
    
- [Propriedade canônica PidLidScriptStream](pidlidscriptstream-canonical-property.md)
    
- [Propriedade canônica PidLidSmartNoAttach](pidlidsmartnoattach-canonical-property.md)
    
- [Propriedade canônica PidLidToDoTitle](pidlidtodotitle-canonical-property.md)
    
- [Propriedade canônica PidLidUseTnef](pidlidusetnef-canonical-property.md)
    
As propriedades nomeadas no namespace **PSETID_Meeting** são as seguintes: 
  
- [Propriedade canônica PidLidMeetingType](pidlidmeetingtype-canonical-property.md)
    
As propriedades nomeadas no namespace **PSETID_Task** são as seguintes: 
  
- [Propriedade canônica PidLidTaskActualEffort](pidlidtaskactualeffort-canonical-property.md)
    
- [Propriedade canônica PidLidTaskDueDate](pidlidtaskduedate-canonical-property.md)
    
- [Propriedade canônica PidLidTaskEstimatedEffort](pidlidtaskestimatedeffort-canonical-property.md)
    
- [Propriedade canônica PidLidTaskFRecurring](pidlidtaskfrecurring-canonical-property.md)
    
- [Propriedade canônica PidLidTaskStartDate](pidlidtaskstartdate-canonical-property.md)
    
- [Propriedade canônica PidLidTaskStatus](pidlidtaskstatus-canonical-property.md)
    
As propriedades nomeadas no namespace **PS_INTERNET_HEADERS** são as seguintes: 
  
- [Propriedade canônica PidTagInternetReturnPath](pidtaginternetreturnpath-canonical-property.md)
    
As propriedades nomeadas no namespace **PSETID_Log** são as seguintes: 
  
- [Propriedade canônica PidLidLogDuration](pidlidlogduration-canonical-property.md)
    
- [Propriedade canônica PidLidLogEnd](pidlidlogend-canonical-property.md)
    
- [Propriedade canônica PidLidLogStart](pidlidlogstart-canonical-property.md)
    
- [Propriedade canônica PidLidLogType](pidlidlogtype-canonical-property.md)
    
As propriedades nomeadas no namespace **PSETID_PUBLIC_STRINGS** são as seguintes: 
  
- [Propriedade canônica PidNameKeywords](pidnamekeywords-canonical-property.md)
    
- [Propriedade canônica PidNameExchangeJunkEmailMoveStamp](pidnameexchangejunkemailmovestamp-canonical-property.md)
    
## <a name="see-also"></a>Confira também



[Constantes de MAPI](mapi-constants.md)
  
[Determinar se o Outlook baixou somente o cabeçalho de uma mensagem](how-to-determine-if-outlook-downloaded-only-the-header-of-a-message.md)
  
[Obter o endereço de email de um item de contato](how-to-get-the-email-address-of-a-contact-item.md)
  
[Remover a definição de formulário personalizada salva com uma mensagem](how-to-remove-custom-form-definition-saved-with-a-message.md)

