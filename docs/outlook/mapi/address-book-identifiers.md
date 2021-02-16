---
title: Identificadores do Address Book
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 40f6c699-86aa-4324-a30d-12c8f1e2de9c
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 822d83c4b77d06c2e000b391c7e229985470ccd3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421568"
---
# <a name="address-book-identifiers"></a>Identificadores do Address Book

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Todos os provedores de agendamento atribuem identificadores de entrada usando a **propriedade PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) a seus objetos de lista de distribuição e usuário de mensagens. Os aplicativos cliente usam esses identificadores de entrada para abrir e acessar os objetos aos quais são atribuídos.
  
O livro de endereços faz uso de três outros tipos de identificadores para representar objetos:
  
- Identificadores de entradas únicas
    
- Identificadores de entrada de modelo único
    
- Identificadores de modelo
    
Devido à variedade de identificadores de entrada e à semelhança com a qual eles são nomeados, é fácil ficar confuso sobre como cada tipo é usado e criado. 
  
Um identificador de entrada único é um identificador de entrada usado para abrir e acessar o tipo de destinatário conhecido como um destinatário único ou personalizado. One-offs are recipients that do not belong to any of the address book providers in the profile. Os identificadores de entrada atribuídos a one-offs usam um formato especificamente reservado para destinatários one-off. Como os identificadores de entrada único são usados para abrir e acessar objetos, eles são armazenados na PR_ENTRYID propriedade.
  
Identificadores de entrada one-offs e one-off são criados:
  
- Quando os usuários de um aplicativo cliente optam por adicionar um destinatário que não representa nenhuma entrada no livro de endereços à lista de destinatários de uma mensagem.
    
- Quando os usuários de um aplicativo cliente optam por adicionar um destinatário que não representa qualquer entrada no livro de endereços a um contêiner modificável do livro de endereços.
    
- Quando um provedor de transporte recebe uma mensagem com um endereço que não pode ser manipulado por seu provedor de agendas de endereços relacionado.
    
- Quando um provedor de transporte recebe uma mensagem com um endereço que pertence a um gateway.
    
Nas duas primeiras situações, o cliente chama **IAddrBook::CreateOneOff** para associar um identificador de entrada único ao destinatário único recém-criado. Nas duas segundas situações, o provedor de transporte chama **IMAPISupport::CreateOneOff** para associar um identificador de entrada único ao endereço estrangeiro. Para obter mais informações, [consulte IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) e [IMAPISupport::CreateOneOff](imapisupport-createoneoff.md).
  
Um identificador de entrada de modelo único é um identificador de entrada de curto prazo que é usado para abrir e acessar um modelo para a criação de one-offs. Os provedores de agendas e os modelos de fornecimento MAPI para inserir as informações necessárias para criar um destinatário de um tipo específico. As informações sobre esses modelos, incluindo seus identificadores de entrada, são publicadas na tabela única. As tabelas one-off são exibidas quando o MAPI chama o método **IABLogon::GetOneOffTable** ou o método **IMAPIProp::OpenProperty** de um contêiner de livro de endereços para solicitar a propriedade **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) ou quando um provedor chama **IMAPISupport::GetOneOffTable**. Para obter mais informações, consulte [IABLogon::GetOneOffTable](iablogon-getoneofftable.md), [IMAPIProp::OpenProperty](imapiprop-openproperty.md)e [IMAPISupport::GetOneOffTable](imapisupport-getoneofftable.md).
  
Para criar um novo one-off, um usuário seleciona um dos modelos listados na tabela única. O cliente passa a coluna PR_ENTRYID da linha selecionada, que é o identificador de entrada de modelo único do modelo selecionado, para **IAddrBook::NewEntry** no parâmetro _lpEIDNewEntryTpl._ Para obter mais informações, consulte [IAddrBook::NewEntry](iaddrbook-newentry.md). O MAPI usa o identificador de entrada de modelo único para exibir o modelo e para permitir que o usuário insira as informações necessárias para criar o destinatário. 
  
Um identificador de modelo é um identificador de entrada que alguns provedores de agendas atribuem a seus destinatários, além do identificador de entrada mantido na propriedade PR_ENTRYID endereço. Os provedores configuram a propriedade **PR_TEMPLATEID** ([PidTagTemplateid)](pidtagtemplateid-canonical-property.md)de um destinatário para armazenar seu identificador de modelo. Alguns provedores de agenda atribuem o mesmo valor para as propriedades do identificador de modelo e do identificador de entrada de um destinatário.
  
Identificadores de modelo são usados apenas por provedores de livro de endereços e por MAPI para vincular dados de destinatário em um provedor, conhecido como provedor de host, para código para o destinatário em outro provedor, chamado de provedor estrangeiro. O provedor de host fornece o armazenamento para o destinatário; o provedor externo fornece a lógica. O processo de associação permite que um provedor de host atualize os dados de um destinatário que ele armazena usando o código de um provedor estrangeiro.
  
Quando o provedor de host está pronto para modificar seu destinatário, ele passa a propriedade PR_TEMPLATEID em uma chamada para o método **IMAPISupport::OpenTemplateID** para iniciar o processo de associação. O MAPI continua o processo transferindo o identificador de modelo para o provedor estrangeiro apropriado por meio de uma chamada para seu método **IABLogon::OpenTemplateID.** Para obter mais informações, [consulte IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) e [IABLogon::OpenTemplateID](iablogon-opentemplateid.md). O provedor estrangeiro retorna um ponteiro para sua implementação **IMAPIProp** para o destinatário, que o provedor de host pode usar no lugar de sua própria implementação. 
  

