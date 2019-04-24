---
title: Recursos necessários para provedores de catálogo de endereços
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e2ccddd7-65e8-41f6-8e21-a4ae98190a96
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 56ca15440c8d323dbab1b6a92a01941106b86934
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328690"
---
# <a name="required-features-for-address-book-providers"></a>Recursos necessários para provedores de catálogo de endereços

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Os provedores de catálogo de endereços podem trabalhar com informações de destinatário temporárias ou permanentes, locais ou remotas, compreensíveis por um ou mais sistemas de mensagens e formatadas para um arquivo de disco ou uma tabela de banco de dados. Há uma variedade de recursos que um provedor de catálogo de endereços pode implementar, adicionando valor e melhorando a interoperabilidade com clientes e outros provedores. No enTanto, alguns recursos são necessários.
  
A tabela a seguir descreve os recursos necessários para todos os provedores de catálogo de endereços e as etapas que você precisa tomar para implementá-los.
  
|**Recurso**|**Como implementar**|
|:-----|:-----|
|Logon da sessão  <br/> | Implementar uma função de ponto de entrada. Para obter mais informações, consulte [implementando uma função de ponto de entrada do provedor de catálogo de endereços](implementing-an-address-book-provider-entry-point-function.md).  <br/>  Implemente o método [IABProvider:: logon](iabprovider-logon.md) . Para obter mais informações, consulte [implementação de logon e logoff do provedor de catálogo de endereços](implementing-address-book-provider-logon-and-logoff.md).  <br/> |
|Logoff de sessão  <br/> |Implemente o método [IABProvider:: Shutdown](iabprovider-shutdown.md) . Para obter mais informações, consulte [implementação de logon e logoff do provedor de catálogo de endereços](implementing-address-book-provider-logon-and-logoff.md).  <br/> |
|Criar identificadores de entrada  <br/> |Fornecer suporte para a propriedade **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)). Para mais informações, consulte [identificadores de entrada MAPI](mapi-entry-identifiers.md) e identificadores de [Catálogo de endereços](address-book-identifiers.md).  <br/> |
|Contribuir para a tabela de status  <br/> | Implemente os métodos apropriados da interface [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) . Para mais informações, consulte [implementação do objeto de status](status-object-implementation.md).  <br/>  Suporta as propriedades da tabela de status necessárias. Para obter mais informações, consulte [tabelas de status](status-tables.md).  <br/>  Chamar [IMAPISupport:: ModifyStatusRow](imapisupport-modifystatusrow.md).  <br/> |
|Fornecer suporte limitado a objetos de status  <br/> | Implemente o método [IMAPIStatus:: ValidateState](imapistatus-validatestate.md) .  <br/>  Retornar MAPI_E_NO_SUPPORT dos outros métodos **IMAPIStatus** .  <br/> |
|Suporte à configuração interativa e programática  <br/> | Implementar uma função de ponto de entrada do serviço de mensagens.  <br/>  Implementar uma tabela de exibição. Para obter mais informações, consulte [Exibir tabelas](display-tables.md) e [exibir a implementação da tabela](display-table-implementation.md).  <br/>  Implemente uma folha de propriedades ou chame o método [IMAPISupport::D oconfigpropsheet](imapisupport-doconfigpropsheet.md) . Para obter mais informações, consulte [implementação da folha de propriedades](property-sheet-implementation.md).  <br/> |
   
Além disso, se o provedor oferecer suporte à criação de destinatários, você deverá fornecer uma lista de modelos de criação. Forneça essa lista implementando o método [IABLogon:: GetOneOffTable](iablogon-getoneofftable.md) para incluir todos os modelos suportados pelo seu provedor e o método [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) de cada contêiner para abrir o **PR_CREATE_TEMPLATES** ([ PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) e inclua todos os modelos suportados pelo contêiner. Para obter mais informações, consulte [implementIng one-off Tables](implementing-one-off-tables.md).
  

