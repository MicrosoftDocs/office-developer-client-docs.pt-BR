---
title: Conexão com manipuladores de eventos personalizados
TOCTitle: Connecting to custom event handlers
ms:assetid: 6e894c16-0fe9-4b86-b798-547b86f44cd8
ms:mtpsurl: https://msdn.microsoft.com/library/Bb610520(v=office.15)
ms:contentKeyID: 55119783
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 31e9a5453bbfbd4a51132fa6af71b86889b4b32e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406103"
---
# <a name="connecting-to-custom-event-handlers"></a>Conexão com manipuladores de eventos personalizados

O Outlook gera eventos para notificar suplementos sobre algo que está acontecendo, como o recebimento de um novo item de email na Caixa de Entrada.  Os suplementos podem especificar para o Outlook que, após a ocorrência de um evento específico, deverão ocorrer certas ações. Este mecanismo de alerta e callback é suportado por representantes do .NET Framework.  Assembly de Interoperabilidade Primária do Outlook (PIA) define representantes aos quais você pode conectar métodos de callback para manipular eventos correspondentes. Este tópico descreve o processo de definir um método de callback e de conectá-lo como um manipulador de eventos para o objeto do Outlook.

## <a name="creating-a-callback-method"></a>Criar um método de callback

Um callback é um método implementado para manipular a ocorrência de um evento específico, e é executado por uma fonte de notificação. No Outlook, os suplementos podem implementar métodos de callback para responder a certos eventos gerados pelo Outlook. O método de callback deve corresponder à assinatura do representante do evento. Por exemplo, para implementar um manipulador de eventos para o evento [ItemSend](https://msdn.microsoft.com/library/bb647198\(v=office.15\)), você precisa declarar o método de callback que corresponde à assinatura do representante correspondente:

```csharp
public delegate void ApplicationEvents_11_ItemSendEventHandler(object Item, ref bool Cancel)
```


```vb
Public Delegate Sub ApplicationEvents_11_ItemSendEventHandler(_
    ByVal Item As Object, ByRef Cancel As Boolean)
```

Ao definir o método de callback, ignore a palavra-chace **Delegate** que, do contrário, definiria outro representante. Uma amostra de método de callback, **MyItemSendEventHandler**, é mostrada abaixo:

```csharp
public void MyItemSendEventHandler(object Item, ref bool Cancel)
```


```vb
Public Sub MyItemSendEventHandler (_
    ByVal Item As Object, ByRef Cancel As Boolean)
…
End Sub
```

## <a name="connecting-a-callback-method"></a>Conexão com um método de callback

Após implementar um método de callback para um evento, você pode conectá-lo ao objeto do Outlook de modo que o Outlook saiba que deve chamar o método como um manipulador de eventos daquele evento. Observe que um evento pode ser manipulado por mais de um manipulador de eventos, e é aqui que entram em jogo os representantes que atribuem a manipulação de eventos a manipuladores de eventos.

Retomando o último exemplo de especificação de um manipulador de eventos para o evento **ItemSend** do objeto **Application**, para conectar **MyItemSendEventHandler** ao objeto **Application** em C\#, crie uma instância do objeto representante, passe **MyItemSendEventHandler** para o construtor do objeto representante e depois adicione este objeto representante ao evento **ItemSend** usando o operador +=:

```csharp
app.ItemSend += new ApplicationEvents_11_ItemSendEventHandler(MyItemSendEventHandler)
```

No Visual Basic, use instrução **AddHandler** para associar o evento **ItemSend** ao manipulador de eventos **MyItemSendEventHandler**:

```vb
AddHandler app.ItemSend, AddressOf MyItemSendEventHandler
```

## <a name="see-also"></a>Confira também

- [Eventos no Outlook PIA](events-in-the-outlook-pia.md)
- [Objetos no Outlook PIA](objects-in-the-outlook-pia.md)

