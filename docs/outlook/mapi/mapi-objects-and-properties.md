---
title: Propriedades e objetos MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0aebf536-dcfb-406d-86ac-65db98c78139
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 7fef84b7519c7a9d6373198283e903fba4fd0780
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411208"
---
# <a name="mapi-objects-and-properties"></a>Propriedades e objetos MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Algumas propriedades são suportadas por muitos tipos diferentes de objetos. As propriedades a seguir são exemplos de propriedades que são usadas por vários objetos:
  
- **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) é um identificador binário usado para abrir objetos.
    
- **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) é uma constante usada para identificar o tipo de objeto.
    
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) é uma cadeia de caracteres usada para descrever um objeto para o usuário.
    
Outras propriedades fazem sentido para um único tipo de objeto. As propriedades a seguir são exemplos de propriedades que se aplicam a um tipo de objeto:
  
- **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) é uma cadeia de caracteres usada para descrever o tipo de uma mensagem.
    
- **PR_ROWID** ([PidTagRowid](pidtagrowid-canonical-property.md)) é um inteiro usado para identificar uma linha em uma tabela.
    
- **PR_ATTACH_SIZE** ([PidTagAttachSize](pidtagattachsize-canonical-property.md)) é um inteiro usado para armazenar o número de bytes em um anexo.
    
Outras propriedades ainda são aplicáveis apenas para um único tipo de objeto em um determinado estado. Propriedades desse tipo são normalmente Propriedades de mensagem. Quando uma mensagem é criada pela primeira vez, seu conjunto de propriedades é muito pequeno. Como ele é enviado por um cliente para um destinatário através do sistema de mensagens, o número de propriedades necessárias para descrever a mensagem aumenta. Algumas dessas propriedades adicionadas aparecem apenas na mensagem à medida que elas são entregues enquanto outras são exibidas apenas na mensagem à medida que ele é enviado. As mensagens também têm propriedades associadas à classe à qual pertencem. Mensagens de relatório, por exemplo, têm propriedades que não são suportadas por mensagens de outras classes, como mensagens de observação. 
  
Cada objeto tem algumas propriedades necessárias e pode ou não ter outras propriedades opcionais. As propriedades obrigatórias são propriedades que devem existir em um objeto antes que o objeto possa ser salvo com êxito com o método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) . Os clientes ou provedores de serviços que usam um objeto podem depender da disponibilidade das propriedades necessárias após a chamada **SaveChanges** . Ou seja, eles podem ter certeza de que uma chamada para o método [IMAPIProp:](imapiprop-getprops.md) : GetProps ou [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) do objeto para recuperar essas propriedades será bem-sucedida. 
  
Propriedades opcionais são propriedades que, dependendo do implementador do objeto, podem ou não ser suportados por um objeto. Um provedor de serviços ou cliente que usa o objeto não pode esperar que as propriedades opcionais estejam disponíveis por meio dos métodos getProps ou **OpenProperty** e sejam definidas como valores válidos. **** 
  
Para uma lista ou propriedades na referência this, consulte [MAPI Properties](mapi-properties.md). As descrições das propriedades pertencentes a cada um dos objetos repositório de mensagens e catálogo de endereços podem ser encontradas na discussão da interface padrão do objeto. Por exemplo, as propriedades de pasta são discutidas com o **IMAPIFolder** e as propriedades do usuário de mensagens são discutidas com o **IMailUser**. As propriedades de mensagens, incluindo as propriedades do relatório de mensagens, são descritas com **IMessage** e na [mensagem de visão geral de propriedades](message-properties-overview.md). As propriedades pertencentes a cada um dos diferentes tipos de tabelas são descritas no tópico [tabelas MAPI](mapi-tables.md) apropriadas. Por exemplo, as propriedades da tabela hierarquia são descritas em [tabelas de hierarquia](hierarchy-tables.md). As propriedades pertencentes a servidores de formulário são descrevem como [escolher o conjunto de propriedades de um formulário](choosing-a-form-s-property-set.md).
  
Quando um cliente ou provedor de serviços chama o método **** GetProps de um objeto para recuperar várias de suas propriedades e uma dessas propriedades não está disponível, GetProps Retorna o aviso MAPI_W_ERRORS_RETURNED. **** A chamada é considerada com êxito porque algumas das propriedades foram retornadas. Quando um cliente ou provedor de serviços **** chama OpenProperty e a propriedade target não está disponível, o método falha com o erro MAPI_E_NOT_FOUND. É importante verificar se uma propriedade solicitada é retornada antes de tentar trabalhar com ela. 
  
Dependendo do objeto, o provedor de serviços que fornece a implementação e a propriedade, uma propriedade pode ter permissão de leitura/gravação ou somente leitura. A permissão de leitura/gravação permite que um cliente ou provedor de serviços usando a propriedade altere seu valor; a permissão somente leitura permite que apenas o provedor de serviços que possui o objeto faça alterações. 
  
Para descobrir exatamente quais propriedades estão atualmente definidas para um objeto, chame [IMAPIProp::](imapiprop-getproplist.md)getproplist. O **** método getproplist permite que um chamador descubra o que está disponível antes de uma tentativa de abrir uma propriedade potencialmente não existente ser feita. Como não há um conjunto padrão de propriedades que todos os objetos de um tipo específico oferecem suporte, é impossível adivinhar se um objeto suporta ou não uma determinada propriedade. Chamar **** getproplist elimina o trabalho de adivinhação. 
  
## <a name="see-also"></a>Confira também



[Propriedades e objetos MAPI](mapi-objects-and-properties.md)

