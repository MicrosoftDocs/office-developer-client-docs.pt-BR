---
title: Identificadores de catálogo de endereços
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 40f6c699-86aa-4324-a30d-12c8f1e2de9c
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 0814d76dac97e40940f41c49dbf72efdd26b3cca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766133"
---
# <a name="address-book-identifiers"></a>Identificadores de catálogo de endereços

  
  
**Aplica-se a**: Outlook 
  
Todos os provedores de catálogo de endereços atribuem identificadores de entrada usando a propriedade **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) para suas mensagens de usuário e os objetos da lista de distribuição. Aplicativos clientes usam esses identificadores de entrada para abrir e acessar os objetos aos quais eles são atribuídos.
  
O catálogo de endereços usa três outros tipos de identificadores para representar objetos:
  
- Identificadores de entrada únicos
    
- Identificadores de entrada do modelo únicos
    
- Identificadores de modelo
    
Devido à variedade de identificadores de entrada e a semelhança com os quais elas são nomeadas, é fácil ficar confusos sobre como cada tipo é usado e criado. 
  
Um identificador de entrada únicos é um identificador de entrada que é usado para abrir e acessar o tipo de destinatário, conhecido como um one-off ou destinatário personalizado. Algo isolado é destinatários que não pertencem a qualquer um dos provedores de catálogo de endereços no perfil. Os identificadores de entrada atribuídos a algo isolado usam um formato reservados especificamente para destinatários únicos. Como os identificadores de entrada únicos são usados para abrir e acessar objetos, eles são armazenados na propriedade PR_ENTRYID.
  
Algo isolado e os identificadores de entrada únicos são criados:
  
- Quando os usuários de um aplicativo cliente optar por adicionar um destinatário que não representa qualquer entrada no catálogo de endereços à lista de destinatários da mensagem.
    
- Quando os usuários de um aplicativo cliente optar por adicionar um destinatário que não representa qualquer entrada no catálogo de endereços para um contêiner de catálogo de endereços pode ser modificado.
    
- Quando um provedor de transporte recebe uma mensagem com um endereço que não pode ser manipulada pelo seu provedor de catálogo de endereços relacionados.
    
- Quando um provedor de transporte recebe uma mensagem com um endereço que pertence a um gateway.
    
Nas duas primeiras situações, o cliente chama **IAddrBook::CreateOneOff** para associar um identificador de entrada únicos o destinatário único recém-criado. O segundo duas situações, o provedor de transporte chama **IMAPISupport::CreateOneOff** para associar um identificador de entrada únicos com o endereço externo. Para obter mais informações, consulte [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) e [IMAPISupport::CreateOneOff](imapisupport-createoneoff.md).
  
Um identificador de modelo únicos de entrada é um identificador de entrada de curto prazo que é usado para abrir e acessar um modelo para criar algo isolado. Provedores de catálogo de endereços e MAPI fornecem modelos para inserindo as informações que é necessário para criar um destinatário de um determinado tipo. Informações sobre esses modelos, incluindo seus identificadores de entrada, são publicadas na tabela único. Tabelas únicas são exibidas ao MAPI chama o método **IABLogon:: GetOneOffTable** ou método **IMAPIProp::OpenProperty** de um contêiner catálogo de endereços para solicitar o **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) propriedade ou quando um provedor chama **IMAPISupport::GetOneOffTable**. Para obter mais informações, consulte [IABLogon:: GetOneOffTable](iablogon-getoneofftable.md), [IMAPIProp::OpenProperty](imapiprop-openproperty.md)e [IMAPISupport::GetOneOffTable](imapisupport-getoneofftable.md).
  
Para criar um one-off novo, um usuário seleciona um dos modelos listados na tabela a one-off. O cliente passa a coluna PR_ENTRYID a linha selecionada, o que é o identificador de entrada do modelo únicos do modelo selecionado, para **IAddrBook::NewEntry** no parâmetro _lpEIDNewEntryTpl_ . Para obter mais informações, consulte [IAddrBook::NewEntry](iaddrbook-newentry.md). MAPI usa o identificador de entrada de modelo únicos para exibir o modelo e para permitir que o usuário insira as informações necessárias para criar o destinatário. 
  
Um identificador de modelo é um identificador de entrada que alguns provedores de catálogo de endereços atribuir aos destinatários além o identificador de entrada que é mantido na propriedade PR_ENTRYID. Provedores de definir a propriedade de **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) de um destinatário para armazenar seu identificador de modelo. Alguns provedores de catálogo de endereços atribuir o mesmo valor para o identificador de modelo de um destinatário e propriedades de identificador de entrada.
  
Identificadores de modelo são usados apenas por provedores de catálogo de endereços e MAPI vincular dados de destinatários em um provedor, conhecidos como o provedor de host, ao código do destinatário em outro provedor, conhecidos como o provedor estrangeiro. O provedor de host fornece o armazenamento para o destinatário; o provedor estrangeiro fornece a lógica. O processo de ligação habilita um provedor de host atualizar os dados de um destinatário que ele armazena usando o código de um provedor de estrangeiro.
  
Quando o provedor de host está pronto para modificar o destinatário, ele passa a propriedade PR_TEMPLATEID em uma chamada para o método **IMAPISupport::OpenTemplateID** para iniciar o processo de ligação. MAPI continua o processo transferindo o identificador de modelo para o provedor estrangeiro apropriado por meio de uma chamada para seu método de **IABLogon:: OpenTemplateID** . Para obter mais informações, consulte [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) e [IABLogon:: OpenTemplateID](iablogon-opentemplateid.md). O provedor estrangeiro retorna um ponteiro para sua implementação **IMAPIProp** para o destinatário, que o provedor de host pode ser usada no lugar de sua própria implementação. 
  

