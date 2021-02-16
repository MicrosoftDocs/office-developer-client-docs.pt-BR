---
title: Recursos necessários para provedores de lista de endereços
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e2ccddd7-65e8-41f6-8e21-a4ae98190a96
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 56ca15440c8d323dbab1b6a92a01941106b86934
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421393"
---
# <a name="required-features-for-address-book-providers"></a>Recursos necessários para provedores de lista de endereços

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Os provedores de agendamento de endereço podem trabalhar com informações de destinatário temporárias ou permanentes, locais ou remotas, compreensíveis por um ou mais sistemas de mensagens e formatadas para um arquivo de disco ou tabela de banco de dados. Há uma variedade de recursos que um provedor de agendas pode implementar, agregando valor e melhorando a interoperabilidade com clientes e outros provedores. No entanto, alguns recursos são necessários.
  
A tabela a seguir descreve os recursos necessários para todos os provedores de agendas e as etapas que você precisa seguir para implementá-los.
  
|**Característica**|**Como implementar**|
|:-----|:-----|
|Logon da sessão  <br/> | Implemente uma função de ponto de entrada. Para obter mais informações, consulte Implementando uma função de ponto de entrada do [provedor de agendamento de endereços.](implementing-an-address-book-provider-entry-point-function.md)  <br/>  Implemente [o método IABProvider::Logon.](iabprovider-logon.md) Para obter mais informações, [consulte Implementando logon](implementing-address-book-provider-logon-and-logoff.md)e logoff do provedor de agendamento de endereço.  <br/> |
|Logoff da sessão  <br/> |Implemente [o método IABProvider::Shutdown.](iabprovider-shutdown.md) Para obter mais informações, [consulte Implementando logon](implementing-address-book-provider-logon-and-logoff.md)e logoff do provedor de agendamento de endereço.  <br/> |
|Criar identificadores de entrada  <br/> |Forneça suporte para a **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)). Para obter mais informações, consulte [Identificadores de entrada MAPI](mapi-entry-identifiers.md) e identificadores [do livro de endereços.](address-book-identifiers.md)  <br/> |
|Contribuir para a tabela de status  <br/> | Implemente os métodos apropriados da interface [IMAPIStatus : IMAPIProp.](imapistatusimapiprop.md) Para obter mais informações, consulte [Implementação de objeto de status](status-object-implementation.md).  <br/>  Suporte às propriedades necessárias da tabela de status. Para obter mais informações, consulte [Tabelas de Status.](status-tables.md)  <br/>  Chame [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md).  <br/> |
|Fornecer suporte ao objeto de status limitado  <br/> | Implemente [o método IMAPIStatus::ValidateState.](imapistatus-validatestate.md)  <br/>  Retorne MAPI_E_NO_SUPPORT dos outros **métodos IMAPIStatus.**  <br/> |
|Suporte à configuração interativa e programática  <br/> | Implemente uma função de ponto de entrada do serviço de mensagens.  <br/>  Implemente uma tabela de exibição. Para obter mais informações, consulte [Display Tables](display-tables.md) and Display [Table Implementation](display-table-implementation.md).  <br/>  Implemente uma folha de propriedades ou chame [o método IMAPISupport::D oConfigPropsheet.](imapisupport-doconfigpropsheet.md) Para obter mais informações, consulte [Implementação da Folha de Propriedades.](property-sheet-implementation.md)  <br/> |
   
Além disso, se seu provedor oferece suporte à criação de destinatários, você deve fornecer uma lista de modelos de criação. Para fornecer essa lista, implemente o método [IABLogon::GetOneOffTable](iablogon-getoneofftable.md) para incluir todos os modelos suportados pelo provedor e o método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) de cada contêiner para abrir a propriedade **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) e incluir todos os modelos com suporte no contêiner. Para obter mais informações, [consulte Implementando One-Off Tabelas.](implementing-one-off-tables.md)
  

