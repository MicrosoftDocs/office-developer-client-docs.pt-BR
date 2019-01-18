---
title: Métodos e propriedade no Outlook PIA
TOCTitle: Methods and properties in the Outlook PIA
ms:assetid: ec7742de-ead6-41dd-90a3-1280fdf09d54
ms:mtpsurl: https://msdn.microsoft.com/library/Bb612528(v=office.15)
ms:contentKeyID: 55119780
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 90c13559094fbffd2dbe9a99602ee235c92d9445
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28723079"
---
# <a name="methods-and-properties-in-the-outlook-pia"></a>Métodos e propriedade no Outlook PIA

Este tópico descreve como acessar métodos e propriedades de um objeto em código gerenciado usando a Assembly de Interoperabilidade Primário do Outlook (PIA).

## <a name="where-helper-objects-come-from"></a>De onde vêm os objetos auxiliares

Para criar o Outlook PIA, o Outlook usa o Importador de Bibliotecas de Tipos (TLBIMP) no .NET Framework para converter definições de tipos da biblioteca de tipos COM em definições equivalentes em um assembly de tempo de execução em linguagem comum (CLR). No COM, um objeto é, de fato, uma co-classe que consiste no seguinte:

- A interface primária (por exemplo, a interface [ \_FormRegion](https://msdn.microsoft.com/library/bb645761\(v=office.15\))).

- A interface de eventos(por exemplo, a interface [FormRegionEvents](https://msdn.microsoft.com/library/bb611940\(v=office.15\))).

O TLBIMP importa a interface primária e a interface de eventos para cada objeto e cria uma quantidade de interfaces, representantes e classes, entre os quais os seguintes:

- A interface de eventos .NET (por exemplo, a interface [FormRegionEvents\_Event](https://msdn.microsoft.com/library/bb647619\(v=office.15\))).

- A classe .NET (por exemplo, a classe [FormRegionClass](https://msdn.microsoft.com/library/bb624204\(v=office.15\))).

- A interface .NET (por exemplo, a interface [FormRegion](https://msdn.microsoft.com/library/bb652633\(v=office.15\))).

## <a name="what-the-helper-objects-are-for"></a>Para que servem os objetos auxiliares

Continuando a usar o objeto **FormRegion** como exemplo, a lista a seguir examina o que contêm cada uma das interfaces e classes listadas anteriormente.

- A interface \_FormRegion define todos os métodos e propriedades de FormRegion. Normalmente, você não usa esta interface em código, exceto na condição descrita abaixo.

- A interface **FormRegionEvents** define métodos de mapeamento para eventos de FormRegion. Não use essa interface com código.

- O TLBIMP também processa a interface **FormRegionEvents** para criar a interface **FormRegionEvents**\_Event que define todos os eventos de FormRegion. Normalmente, você não usa esta interface em código, exceto na condição descrita abaixo.

- A classe FormRegionClass define todos os membros de métodos, propriedades e eventos de FormRegion. Esta é a classe à qual a interface FormRegion é atribuída para associar-se com os bastidores, de modo que você possa escrever um código para criar uma instância da interface FormRegion. Porém, você não deve usar essa interface diretamente em código.

- A interface FormRegion herda a interface \_FormRegion interface e a interface**FormRegionEvents**\_Event. A Figura 1 ilustra esta relação de herança.
    
  **Figura 1. A interface FormRegion herda métodos e propriedades da interface \_FormRegion e herda eventos da interface FormRegionEvents\_Event**

  ![Figura 1. A interface FormRegion herda métodos e propriedades da interface _FormRegion e herda eventos da interface FormRegionEvents_Event](media/pia-form-region-interface.gif)
    
  Normalmente, FormRegion é a única interface que você usa em código gerenciado para acessar o objeto e os membros de método, propriedade e evento do objeto **FormRegion**.

Usando o objeto **Application** como outro exemplo, você acessa o objeto **Application**, métodos, propriedade e eventos através da interface [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\)). Entretanto, existem três exceções nas quais você deve usar uma interface diferente ou, dependendo da linguagem, você desejaria usar uma interface diferente:

- Quando você acessa um método que compartilha o mesmo nome de um evento, uma prática recomendada é converter a interface primária para chamar o método. Por exemplo, o objeto **Application** tem um método [Quit](https://msdn.microsoft.com/library/bb646614\(v=office.15\)) e um evento[Quit](https://msdn.microsoft.com/library/bb622595\(v=office.15\)). No Visual Basic .NET, você pode acessar o método Quit através da interface Application. Em C\#, é possível evitar um aviso do compilador ao converter o método Quit para a interface primária, como mostrado na seguinte amostra de código:
    
   ```csharp
      void DemoApp()
      {
          Outlook.Application myApp = new Outlook.Application();
          // Other application code here
          ((Outlook._Application)myApp).Quit();
      }
   ```

- Quando você acessa um evento que compartilha o mesmo nome de um método daquele objeto, você deve converter a interface de eventos apropriada para conectar-se com o evento. Semelhante ao exemplo acima, para se conectar ao evento Quit, converta para a interface [ApplicationEvents\_11\_Event](https://msdn.microsoft.com/library/bb622725\(v=office.15\)).

- Quando você se conectar a uma versão anterior de um evento foi estendida posteriormente em uma versão posterior do Outlook, você deve se conectar à versão do evento na interface anterior. Por exemplo, se você deseja se conectar à versão do evento Quit para o objeto **Application** implementado para Outlook 2002 em vez da versão mais recente, conecte-se ao evento [Quit](https://msdn.microsoft.com/library/bb609660\(v=office.15\)) definido para a interface[ApplicationEvents\_10\_Event](https://msdn.microsoft.com/library/bb610098\(v=office.15\)) em vez do evento definido na interface ApplicationEvents\_11\_Event.

## <a name="see-also"></a>Confira também

- [Associar o Outlook PIA ao modelo de objeto](relating-the-outlook-pia-with-the-object-model.md)
- [Objetos no Outlook PIA](objects-in-the-outlook-pia.md)
- [Eventos no Outlook PIA](events-in-the-outlook-pia.md)

