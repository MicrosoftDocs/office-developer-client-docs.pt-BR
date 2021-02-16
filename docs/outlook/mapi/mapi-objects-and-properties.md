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
  
Algumas propriedades são suportadas por vários tipos diferentes de objetos. As propriedades a seguir são exemplos de propriedades usadas por vários objetos:
  
- **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) é um identificador binário usado para abrir objetos.
    
- **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) é uma constante usada para identificar o tipo de objeto.
    
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) é uma cadeia de caracteres usada para descrever um objeto para o usuário.
    
Outras propriedades fazem sentido para um único tipo de objeto. As propriedades a seguir são exemplos de propriedades que se aplicam a um tipo de objeto:
  
- **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) é uma cadeia de caracteres usada para descrever o tipo de uma mensagem.
    
- **PR_ROWID** ([PidTagRowid](pidtagrowid-canonical-property.md)) é um inteiro usado para identificar uma linha em uma tabela.
    
- **PR_ATTACH_SIZE** ([PidTagAttachSize](pidtagattachsize-canonical-property.md)) é um número inteiro usado para armazenar o número de bytes em um anexo.
    
Ainda assim, outras propriedades são aplicáveis apenas a um único tipo de objeto em um estado específico. Propriedades desse tipo normalmente são propriedades de mensagem. Quando uma mensagem é criada pela primeira vez, seu conjunto de propriedades é muito pequeno. Como ele é enviado por um cliente para um destinatário por meio do sistema de mensagens, o número de propriedades necessárias para descrever a mensagem aumenta. Algumas dessas propriedades adicionadas aparecem somente na mensagem à medida que ela está sendo entregue, enquanto outras aparecem apenas na mensagem enquanto ela está sendo enviada. As mensagens também têm propriedades associadas à classe à qual pertencem. As mensagens de relatório, por exemplo, têm propriedades que não são suportadas por mensagens de outras classes, como mensagens de anotação. 
  
Cada objeto tem algumas propriedades necessárias e pode ou não ter outras propriedades opcionais. Propriedades necessárias são propriedades que devem existir em um objeto antes que o objeto possa ser salvo com êxito com seu método [IMAPIProp::SaveChanges.](imapiprop-savechanges.md) Clientes ou provedores de serviços que usam um objeto podem depender da disponibilidade das propriedades necessárias após a **chamada de SaveChanges.** Ou seja, eles podem ter certeza de que uma chamada para o método [IMAPIProp::GetProps](imapiprop-getprops.md) do objeto ou o método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) para recuperar essas propriedades terá êxito. 
  
Propriedades opcionais são propriedades que, dependendo do implementador do objeto, podem ou não ter suporte de um objeto. Um cliente ou provedor de serviços que usa o objeto não pode esperar que as propriedades opcionais sejam disponibilizadas por meio dos métodos **GetProps** ou **OpenProperty** e sejam definidas como valores válidos. 
  
For a list or properties in the this Reference, see [MAPI Properties](mapi-properties.md). Descrições das propriedades pertencentes a cada um dos objetos de armazenamento de mensagens e de address book podem ser encontradas na discussão sobre a interface padrão do objeto. Por exemplo, as propriedades de pasta são discutidas com **IMAPIFolder** e as propriedades de usuário de mensagens são discutidas com **IMailUser**. As propriedades da mensagem, incluindo as propriedades da mensagem de relatório, são descritas com **IMessage** e em [Message Properties Overview](message-properties-overview.md). As propriedades pertencentes a cada um dos diferentes tipos de tabelas são descritas no tópico [mapi tables](mapi-tables.md) apropriado. Por exemplo, as propriedades da tabela de hierarquias são descritas em [Tabelas de Hierarquia.](hierarchy-tables.md) Propriedades pertencentes a servidores de formulário estão descrevendo [em Escolhendo um conjunto de propriedades do formulário.](choosing-a-form-s-property-set.md)
  
Quando um cliente ou provedor de serviços chama o método **GetProps** de um objeto para recuperar várias de suas propriedades e uma dessas propriedades está indisponível, **GetProps** retorna o aviso MAPI_W_ERRORS_RETURNED. A chamada é considerada bem-sucedida porque algumas das propriedades foram retornadas. Quando um cliente ou provedor de serviços chama **OpenProperty** e a propriedade de destino não está disponível, o método falha com o erro MAPI_E_NOT_FOUND. É importante verificar se uma propriedade solicitada é retornada antes de tentar trabalhar com ela. 
  
Dependendo do objeto, do provedor de serviços que fornece a implementação e da propriedade, uma propriedade pode ter permissão de leitura/gravação ou somente leitura. A permissão de leitura/gravação permite que um cliente ou provedor de serviços que use a propriedade altere seu valor; A permissão somente leitura permite que apenas o provedor de serviços que possui o objeto faça alterações. 
  
Para descobrir exatamente quais propriedades estão definidas no momento para um objeto, chame [IMAPIProp::GetPropList](imapiprop-getproplist.md). O **método GetPropList** permite que um chamador descubra o que está disponível antes que seja feita uma tentativa de abrir uma propriedade potencialmente inexistente. Como não há um conjunto padrão de propriedades compatíveis com todos os objetos de um tipo específico, é impossível adivinhar se um objeto oferece suporte ou não a uma propriedade específica. Chamar **GetPropList** elimina o trabalho de suposição. 
  
## <a name="see-also"></a>Confira também



[Propriedades e objetos MAPI](mapi-objects-and-properties.md)

