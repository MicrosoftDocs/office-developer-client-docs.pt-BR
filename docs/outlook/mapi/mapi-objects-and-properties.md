---
title: Propriedades e objetos MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0aebf536-dcfb-406d-86ac-65db98c78139
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 0efc111523ad285d54fc40e37fe83a1130f1d291
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767899"
---
# <a name="mapi-objects-and-properties"></a>Propriedades e objetos MAPI

  
  
**Aplica-se a**: Outlook 
  
Algumas propriedades são compatíveis com muitos tipos diferentes de objetos. As propriedades a seguir são exemplos de propriedades que são utilizadas por vários objetos:
  
- **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) é um identificador binário usado para abrir os objetos.
    
- **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) é uma constante usada para identificar o tipo de objeto.
    
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) é uma cadeia de caracteres usada para descrever um objeto para o usuário.
    
Outras propriedades fazem sentido para um único tipo de objeto. As propriedades a seguir são exemplos de propriedades que se aplicam a um tipo de objeto:
  
- **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) é uma cadeia de caracteres usada para descrever o tipo de uma mensagem.
    
- **PR_ROWID** ([PidTagRowid](pidtagrowid-canonical-property.md)) é um inteiro usado para identificar uma linha em uma tabela.
    
- **PR_ATTACH_SIZE** ([PidTagAttachSize](pidtagattachsize-canonical-property.md)) é um inteiro usado para armazenar o número de bytes em um anexo.
    
Ainda outras propriedades são aplicáveis somente para um único tipo de objeto em um determinado estado. Propriedades desse tipo são geralmente propriedades da mensagem. Quando uma mensagem é criada pela primeira vez, seu conjunto de propriedades é muito pequeno. Como ele é enviado por um cliente para um destinatário por meio do sistema de mensagens, aumenta o número de propriedades necessárias para descrever a mensagem. Algumas dessas propriedades adicionadas aparecem apenas na mensagem conforme ele está sendo entregue enquanto outras pessoas aparecem apenas na mensagem, conforme ele está sendo enviado. Mensagens também têm propriedades que estão associadas a classe às quais eles pertencem. Mensagens de relatório, por exemplo, têm propriedades que não são suportadas pelo mensagens de outras classes, como mensagens de nota. 
  
Cada objeto tem algumas propriedades necessárias e pode ou não ter outras propriedades opcionais. Propriedades necessárias são propriedades devem existir em um objeto antes do objeto pode ser salva com êxito com seu método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) . Clientes ou provedores de serviço usando um objeto podem depender a disponibilidade das propriedades necessárias após a chamada **SaveChanges** . Ou seja, eles podem ser certeza de que uma chamada para o método [IMAPIProp::GetProps](imapiprop-getprops.md) do objeto ou o método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) para recuperar essas propriedades terá êxito. 
  
Propriedades opcionais são propriedades que, dependendo do implementador do objeto, pode ou não podem ser suportadas por um objeto. Um provedor de cliente ou de serviço usando o objeto não pode esperar propriedades opcionais esteja disponível por meio dos métodos **GetProps** ou **OpenProperty** e seja definida como valores válidos. 
  
Para uma lista ou propriedades em esta referência, consulte [Propriedades MAPI](mapi-properties.md). Descrições das propriedades pertencentes a cada da mensagem armazenam e objetos de catálogo de endereços que podem ser encontrados na discussão de interface de padrão do objeto. Por exemplo, as propriedades da pasta são discutidas com **IMAPIFolder** e mensagens de propriedades de usuário são abordadas com **IMailUser**. Propriedades da mensagem, incluindo propriedades de mensagem do relatório, são descritas com **IMessage** e em [Visão geral das propriedades de mensagem](message-properties-overview.md). Propriedades que pertencem a cada um dos tipos diferentes de tabelas são descritas no tópico apropriado de [Tabelas de MAPI](mapi-tables.md) . Por exemplo, as propriedades da tabela de hierarquia são descritas nas [Tabelas de hierarquia](hierarchy-tables.md). Propriedades que pertencem aos servidores de formulário são descrevendo na [Escolha de propriedade definida um formulário](choosing-a-form-s-property-set.md).
  
Quando um cliente ou serviço provedor chama um método do objeto **GetProps** para recuperar várias de suas propriedades e uma dessas propriedades não estiver disponível, **GetProps** retorna o aviso MAPI_W_ERRORS_RETURNED. A chamada é considerada seja bem sucedido, pois algumas das propriedades foram retornadas. Quando um cliente ou chamadas de provedor de serviço **OpenProperty** e a propriedade de destino estiver indisponível, o método falhar com o erro E_NOT_FOUND. É importante verificar se uma propriedade solicitada é retornada antes de tentar trabalhar com ele. 
  
Dependendo do objeto, o provedor de serviços, fornecendo a implementação e a propriedade, uma propriedade pode ter permissão somente leitura ou leitura/gravação. Permissão de leitura/gravação permite que um provedor de cliente ou serviço que usa a propriedade para alterar seu valor; permissão somente leitura permite que apenas o provedor de serviços ao qual pertence o objeto fazer alterações. 
  
Para saber exatamente quais propriedades estão definidas para um objeto, chame [IMAPIProp::GetPropList](imapiprop-getproplist.md). O método **GetPropList** permite que um chamador Descubra o que há disponível antes da tentativa de abrir uma propriedade potencialmente inexistente. Como não há nenhum conjunto padrão das propriedades que oferecem suporte a todos os objetos de um tipo específico, é impossível de adivinhar ou não um objeto oferece suporte a uma propriedade específica. Chamar **GetPropList** elimina as suposições. 
  
## <a name="see-also"></a>Confira também



[Propriedades e objetos MAPI](mapi-objects-and-properties.md)

