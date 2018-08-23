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
ms.openlocfilehash: 919b21490bb3b4418ba291e8e06198028c995b00
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570867"
---
# <a name="required-features-for-address-book-providers"></a>Recursos necessários para provedores de catálogo de endereços

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Provedores de catálogo de endereços podem trabalhar com as informações de destinatário é temporário ou permanente, local ou remoto, compreensível por um ou mais sistemas de mensagens e formatada para uma tabela de banco de dados ou arquivo de disco. Há uma variedade de recursos que um provedor de catálogo de endereços pode implementar, assim, adicionando valor e melhorar a interoperabilidade com clientes e outros provedores. No entanto, alguns recursos que são necessários.
  
A tabela a seguir descreve os recursos necessários de todos os provedores de catálogo de endereços e as etapas que precisam ser executadas para implementá-las.
  
|**Recurso**|**Como implementar**|
|:-----|:-----|
|Logon de sessão  <br/> | Implemente uma função de ponto de entrada. Para obter mais informações, consulte [Implementando uma função de ponto de entrada do endereço livro provedor](implementing-an-address-book-provider-entry-point-function.md).  <br/>  Implemente o método [IABProvider::Logon](iabprovider-logon.md) . Para obter mais informações, consulte [Implementando Logon do fornecedor de catálogo de endereços e o Logoff](implementing-address-book-provider-logon-and-logoff.md).  <br/> |
|Fazer logoff de sessão  <br/> |Implemente o método [IABProvider::Shutdown](iabprovider-shutdown.md) . Para obter mais informações, consulte [Implementando Logon do fornecedor de catálogo de endereços e o Logoff](implementing-address-book-provider-logon-and-logoff.md).  <br/> |
|Criar identificadores de entrada  <br/> |Oferecem suporte para a propriedade **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)). Para obter mais informações, consulte [Identificadores de entrada de MAPI](mapi-entry-identifiers.md) e [Identificadores de catálogo de endereços](address-book-identifiers.md).  <br/> |
|Contribuir para a tabela de status  <br/> | Implementar os métodos apropriados do [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) interface. Para obter mais informações, consulte [Implementação do objeto de Status](status-object-implementation.md).  <br/>  Suporte para as propriedades da tabela de status obrigatório. Para obter mais informações, consulte as [Tabelas de Status](status-tables.md).  <br/>  Chame [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md).  <br/> |
|Fornecer suporte do objeto limitado do status  <br/> | Implemente o método [IMAPIStatus::ValidateState](imapistatus-validatestate.md) .  <br/>  Retorne MAPI_E_NO_SUPPORT de outros métodos **IMAPIStatus** .  <br/> |
|Configuração interativa e programática de suporte  <br/> | Implemente uma função de ponto de entrada de serviço de mensagens.  <br/>  Implemente uma tabela de exibição. Para obter mais informações, consulte [As tabelas de exibição](display-tables.md) e a [Implementação da tabela de exibição](display-table-implementation.md).  <br/>  Implementar uma folha de propriedades ou chamar o método [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) . Para obter mais informações, consulte [Implementação da folha de propriedade](property-sheet-implementation.md).  <br/> |
   
Além disso, se o provedor oferece suporte a criação de destinatário, você deverá fornecer uma lista de modelos de criação. Fornecer essa lista por meio da implementação do método [IABLogon:: GetOneOffTable](iablogon-getoneofftable.md) para incluir todos os modelos suportados pelo seu provedor e o método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) de cada contêiner para abrir o **PR_CREATE_TEMPLATES** ([ PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) propriedade e incluir todos os modelos suportados pelo contêiner. Para obter mais informações, consulte [Implementando únicos Tables](implementing-one-off-tables.md).
  

