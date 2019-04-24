---
title: Identificadores do catálogo de endereços
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 40f6c699-86aa-4324-a30d-12c8f1e2de9c
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 822d83c4b77d06c2e000b391c7e229985470ccd3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331091"
---
# <a name="address-book-identifiers"></a>Identificadores do catálogo de endereços

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Todos os provedores de catálogo de endereços atribuem identificadores de entrada usando a propriedade **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) para seus usuários de mensagens e objetos de lista de distribuição. Os aplicativos cliente usam esses identificadores de entrada para abrir e acessar os objetos aos quais são atribuídos.
  
O catálogo de endereços faz uso de três outros tipos de identificadores para representar objetos:
  
- Identificadores de entradas únicas
    
- Identificadores de entrada de modelo únicos
    
- Identificadores de modelo
    
Devido à variedade de identificadores de entrada e à semelhança com a qual eles são nomeados, é fácil se confundir sobre como cada tipo é usado e criado. 
  
Um identificador de entrada one-off é um identificador de entrada que é usado para abrir e acessar o tipo de destinatário conhecido como um destinatário individual ou personalizado. Um-offs são destinatários que não pertencem a nenhum dos provedores de catálogo de endereços no perfil. Os identificadores de entrada atribuídos a um-offs usam um formato reservado especificamente para destinatários únicos. Como os identificadores de entrada únicos são usados para abrir e acessar objetos, eles são armazenados na propriedade PR_ENTRYID.
  
Os identificadores de entrada de um e de um são criados:
  
- Quando usuários de um aplicativo cliente optam por adicionar um destinatário que não representa nenhuma entrada no catálogo de endereços para a lista de destinatários de uma mensagem.
    
- Quando usuários de um aplicativo cliente optam por adicionar um destinatário que não representa nenhuma entrada no catálogo de endereços para um contêiner de catálogo de endereços modificável.
    
- Quando um provedor de transporte recebe uma mensagem com um endereço que não pode ser manipulado por seu provedor de catálogo de endereços relacionado.
    
- Quando um provedor de transporte recebe uma mensagem com um endereço que pertence a um gateway.
    
Nas duas primeiras situações, o cliente chama **IAddrBook:: CreateOneOff** para associar um identificador de entrada one-off ao destinatário one-off recém-criado. Nas segunda duas situações, o provedor de transporte chama **IMAPISupport:: CreateOneOff** para associar um identificador de entrada one-off ao endereço externo. Para obter mais informações, consulte [IAddrBook:: CreateOneOff](iaddrbook-createoneoff.md) e [IMAPISupport:: CreateOneOff](imapisupport-createoneoff.md).
  
Um identificador de entrada de modelo one-off é um identificador de entrada de curto prazo usado para abrir e acessar um modelo para a criação de um. Os provedores do catálogo de endereços e os modelos de fornecimento MAPI para inserir as informações necessárias para criar um destinatário de um tipo específico. As informações sobre esses modelos, incluindo seus identificadores de entrada, são publicadas na tabela única. As tabelas únicas são exibidas quando o MAPI chama o método **IABLogon:: GetOneOffTable** ou um contêiner de catálogo de endereços **IMAPIProp:: OpenProperty** para solicitar o **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) ou quando um provedor chama **IMAPISupport:: GetOneOffTable**. Para obter mais informações, consulte [IABLogon:: GetOneOffTable](iablogon-getoneofftable.md), [IMAPIProp:: OpenProperty](imapiprop-openproperty.md)e [IMAPISupport:: GetOneOffTable](imapisupport-getoneofftable.md).
  
Para criar um novo one-off, um usuário seleciona um dos modelos listados na tabela one-off. O cliente passa a coluna PR_ENTRYID da linha selecionada, que é o identificador de entrada de modelo one-off do modelo selecionado, para **IAddrBook:: NewEntry** no parâmetro _lpEIDNewEntryTpl_ . Para obter mais informações, consulte [IAddrBook:: NewEntry](iaddrbook-newentry.md). MAPI usa o identificador de entrada de modelo one-off para exibir o modelo e permitir que o usuário insira as informações necessárias para criar o destinatário. 
  
Um identificador de modelo é um identificador de entrada que alguns provedores de catálogo de endereços atribuem aos destinatários, além do identificador de entrada que é mantido na propriedade PR_ENTRYID. Os provedores definem a propriedade **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) de um destinatário para armazenar seu identificador de modelo. Alguns provedores de catálogo de endereços atribuem o mesmo valor para o identificador de modelo de um destinatário e propriedades de identificador de entrada.
  
Os identificadores de modelo são usados apenas por provedores de catálogo de endereços e por MAPI para vincular dados de destinatário em um provedor, chamado de provedor de host, para o código do destinatário em outro provedor, chamado de provedor estrangeiro. O provedor de host fornece o armazenamento para o destinatário; o provedor estrangeiro fornece a lógica. O processo de associação permite que um provedor de host atualize os dados de um destinatário que armazena usando o código de um provedor estrangeiro.
  
Quando o provedor de host estiver pronto para modificar seu destinatário, ele passará a propriedade PR_TEMPLATEID em uma chamada para o método **IMAPISupport:: OpenTemplateID** para iniciar o processo de associação. O MAPI continua o processo transferindo o identificador de modelo para o provedor estrangeiro apropriado por meio de uma chamada para o método **IABLogon:: OpenTemplateID** . Para obter mais informações, consulte [IMAPISupport:: OpenTemplateID](imapisupport-opentemplateid.md) e [IABLogon:: OpenTemplateID](iablogon-opentemplateid.md). O provedor estrangeiro retorna um ponteiro para sua implementação **IMAPIProp** para o destinatário, que o provedor de host pode usar no lugar de sua própria implementação. 
  

