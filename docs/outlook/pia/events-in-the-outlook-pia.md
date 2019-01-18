---
title: Eventos no Outlook PIA
TOCTitle: Events in the Outlook PIA
ms:assetid: 1f9eafb3-6645-4e27-81fa-5d73bf94ae40
ms:mtpsurl: https://msdn.microsoft.com/library/office/bb644571(v=office.15)
ms:contentKeyID: 55119782
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 29217a633c02390587a370847291ef62d5621ce8
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699209"
---
# <a name="events-in-the-outlook-pia"></a>Eventos no Outlook PIA

Ao navegar no Assembly de interoperabilidade primária (PIA) do Outlook, você notará que muitas interfaces e representantes de eventos têm nomes familiares de objetos e eventos no modelo de objeto do Outlook. Ao contrário dos eventos na biblioteca do tipo COM, os eventos no Outlook PIA não são definidos na mesma interface como nos métodos e propriedades do mesmo objeto. Interfaces, representantes e classes sink helper relacionados a eventos são importados ou criados para oferecer suporte a eventos no Outlook PIA. Este tópico descreve essas interfaces, representantes e classes sink helper relacionados a eventos.

## <a name="where-do-the-event-interfaces-delegates-and-sink-helper-classes-come-from"></a>De onde vêm as interfaces, representantes e classes Sink Helper de eventos

Para criar o Outlook PIA, o Outlook usa o Importador de bibliotecas de tipos (TLBIMP) no .NET Framework para converter definições de tipos da biblioteca de tipos COM em definições equivalentes em um assembly de tempo de execução em linguagem comum (CLR). O TLBIMP importa estes dois tipos de interfaces para cada objeto:

  - A interface primária (por exemplo, a interface [\_Application](https://msdn.microsoft.com/library/bb611255\(v=office.15\)))

  - A interface do evento (por exemplo, a interface [ApplicationEvents\_11](https://msdn.microsoft.com/library/bb609229\(v=office.15\)))

O TLBIMP processa as interfaces importadas e cria diversos representantes, interfaces e classes, incluindo a interface do .NET (por exemplo, a interface [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\))). Se o objeto tiver eventos, é criado o seguinte:

  - A interface do evento .NET (por exemplo, a interface [ApplicationEvents\_11\_Event](https://msdn.microsoft.com/library/bb622725\(v=office.15\)))

  - O representante de cada evento (por exemplo, o representante [ApplicationEvents\_11\_ItemSendEventHandler](https://msdn.microsoft.com/library/bb610818\(v=office.15\)))

  - A classe do sink helper (por exemplo, a classe [ApplicationEvents\_11\_SinkHelper](https://msdn.microsoft.com/library/bb609842\(v=office.15\)))

### <a name="multiple-versions-of-events"></a>Várias versões de eventos

Alguns objetos que existiram para várias versões do Outlook têm diferentes implementações de eventos ao longo das versões, e tiveram mais eventos adicionados à medida que as novas versões foram lançadas. Para oferecer suporte a eventos que variam pelas diversas versões, o Outlook distingue essas interfaces, representantes e classes relacionados a eventos adicionando um número de versão a seus nomes. Por exemplo:

  - As interfaces de eventos importadas do objeto **Application** incluem:
    
      - A versão mais antiga para Outlook 98 e Outlook 2000: a interface [ApplicationEvents](https://msdn.microsoft.com/library/bb644093\(v=office.15\))
    
      - A versão do Outlook 2002: a interface [ApplicationEvents\_10](https://msdn.microsoft.com/library/bb647702\(v=office.15\))
    
      - A versão do Outlook 2003 e versões posteriores: a interface [ApplicationEvents\_11](https://msdn.microsoft.com/library/bb609229\(v=office.15\))

  - As interfaces de evento .NET criadas por TLBIMP para o objeto **Application** incluem:
    
      - A versão mais antiga para Outlook 98 e Outlook 2000: a interface [ApplicationEvents\_Event](https://msdn.microsoft.com/library/bb609380\(v=office.15\))
    
      - A versão do Outlook 2002: a interface [ApplicationEvents\_10\_Event](https://msdn.microsoft.com/library/bb610098\(v=office.15\))
    
      - A versão do Outlook 2003 e versões posteriores: a interface [ApplicationEvents\_11\_Event](https://msdn.microsoft.com/library/bb622725\(v=office.15\))

  - Os representantes que o TLBIMP cria para cada evento em cada versão do objeto **Application**, por exemplo, um representante para cada versão do evento ItemSend:
    
      - A versão mais antiga para Outlook 98 e Outlook 2000: o representante [ApplicationEvents\_ItemSendEventHandler](https://msdn.microsoft.com/library/bb622515\(v=office.15\))
    
      - A versão para Outlook 2002: o representante [ApplicationEvents\_10\_ItemSendEventHandler](https://msdn.microsoft.com/library/bb646436\(v=office.15\))
    
      - A versão para Outlook 2003 e posteriores: o representante [ApplicationEvents\_11\_ItemSendEventHandler](https://msdn.microsoft.com/library/bb610818\(v=office.15\))

Logicamente, os eventos adicionados a uma versão posterior não serão exibidos nas interfaces de eventos de versões anteriores e não terão representantes correspondentes nas versões anteriores. Por exemplo, o evento [AttachmentSelectionChange](https://msdn.microsoft.com/library/ff184926\(v=office.15\)) foi adicionado ao objeto [Explorer](https://msdn.microsoft.com/library/bb623678\(v=office.15\)) no Outlook 2010, portanto, não faz parte das interfaces de eventos anteriores para o objeto Explorer:

  - Interface ExplorerEvents

  - Interface ExplorerEvents\_Event

Por outro lado, você pode encontrar o evento na interface de evento mais recente do .NET, ExplorerEvents\_10\_Event, e seu representante para a versão do Outlook 2010, [ExplorerEvents\_10\_AttachmentSelectionChangeEventHandler](https://msdn.microsoft.com/library/ff185177\(v=office.15\)).

## <a name="what-the-event-interfaces-delegates-and-sink-helper-classes-are-for"></a>Para que servem as interfaces, representantes e classes do Sink Helper de eventos

Usando o objeto **Application** como um exemplo, esta seção descreve o que cada interface e classe listada acima contém:

  - A interface principal, \_Application, define todos os métodos e propriedades do Aplicativo. Exceto por uma condição descrita abaixo, normalmente não se usa esta interface em código.

  - As interfaces de eventos importadas por TLBIMP, como ApplicationEvents\_11 e ApplicationEvents\_10, definem o mapeamento dos métodos para eventos do Aplicativo na versão correspondente do Outlook. Não use essa interface com código.

  - As interfaces de eventos criadas por TLBIMP, como ApplicationEvents\_11\_Event e ApplicationEvents\_10\_Event, definem o mapeamento dos métodos para eventos do Aplicativo na versão correspondente do Outlook. Ao criar um manipulador de eventos para um evento em uma versão específica, você implementa o manipulador de eventos como um método e conecta o método ao evento definido na versão correspondente da interface de eventos do .NET. Exceto por uma condição descrita abaixo, normalmente não se faz referência a esta interface de eventos em código.

  - A interface do .NET, Application, herda as interfaces \_Application e ApplicationEvents\_11\_Event. Normalmente, esta é a única interface que se usa em código gerenciado para acessar o objeto, método, propriedade e os membros do evento do objeto **Application**. Entretanto, há duas exceções em que não se usa a interface do .NET, mas sim interfaces diferentes para se conectar a um evento:
    
      - Ao acessar um evento que compartilha o mesmo nome como um método daquele objeto, converta a interface de eventos apropriada para conectar-se ao evento. Por exemplo, para se conectar ao evento [Quit](https://msdn.microsoft.com/library/bb622595\(v=office.15\)), converta para a interface ApplicationEvents\_11\_Event.
    
      - Ao se conectar a uma versão anterior de um evento que tenha sido estendida em uma versão posterior do Outlook, você deve se conectar à versão do evento na interface anterior. Por exemplo, se você quiser se conectar à versão do evento Quit para o objeto **Application** implementado para o Outlook 2002 em vez da versão mais recente, conecte-se ao evento [Quit](https://msdn.microsoft.com/library/bb609660\(v=office.15\)) definido para a interface ApplicationEvents\_10\_Event ao invés do evento Quit definido na interface ApplicationEvents\_11\_Event.

  - Representantes fornecem uma estrutura para você criar os manipuladores de eventos personalizados para eventos específicos em uma versão específica do Outlook. Por exemplo, se quiser adicionar a verificação da existência de uma linha de assunto em um item do Outlook antes de enviá-lo, implemente a verificação em um método de retorno de chamada que tenha a mesma assinatura como representante, ApplicationEvents\_11\_ ItemSendEventHandler. Depois conecte o método de retorno de chamada como um manipulador de eventos para o evento ItemSend definido na interface ApplicationEvents\_11\_Event. Para saber mais sobre como conectar o método de retorno de chamada como um manipulador de eventos para um objeto, consulte [Conectar a manipuladores de eventos personalizados](connecting-to-custom-event-handlers.md).

  - As classes sink helper criadas pelo TLBIMP, por exemplo, ApplicationEvents\_11\_SinkHelper e [ApplicationEvents\_10\_SinkHelper](https://msdn.microsoft.com/library/bb644070\(v=office.15\)), são objetos de ajuda para eventos do Aplicativo na versão correspondente do Outlook. Não use essas classes no código.

## <a name="see-also"></a>Confira também

- [Associar o Outlook PIA ao modelo de objeto](relating-the-outlook-pia-with-the-object-model.md)
- [Objetos no Outlook PIA](objects-in-the-outlook-pia.md)
- [Métodos e propriedade no Outlook PIA](methods-and-properties-in-the-outlook-pia.md)
- [Desenvolvimento de suplementos gerenciados do Outlook usando o Outlook PIA](developing-managed-outlook-add-ins-using-the-outlook-pia.md)

