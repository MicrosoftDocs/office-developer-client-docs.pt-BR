---
title: Conexão com manipuladores de eventos personalizados
TOCTitle: Connecting to custom event handlers
ms:assetid: 6e894c16-0fe9-4b86-b798-547b86f44cd8
ms:mtpsurl: https://msdn.microsoft.com/library/Bb610520(v=office.15)
ms:contentKeyID: 55119783
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 58722b8b140f89f0fe29a3e52db578a423a0160a
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28711795"
---
# <a name="connecting-to-custom-event-handlers"></a><span data-ttu-id="b9fc5-102">Conexão com manipuladores de eventos personalizados</span><span class="sxs-lookup"><span data-stu-id="b9fc5-102">Connecting to custom event handlers</span></span>

<span data-ttu-id="b9fc5-103">O Outlook gera eventos para notificar suplementos sobre algo que está acontecendo, como o recebimento de um novo item de email na Caixa de Entrada.</span><span class="sxs-lookup"><span data-stu-id="b9fc5-103">Outlook raises events to notify add-ins about something happening, such as the Inbox receiving a new mail item.</span></span> <span data-ttu-id="b9fc5-104"> Os suplementos podem especificar para o Outlook que, após a ocorrência de um evento específico, deverão ocorrer certas ações.</span><span class="sxs-lookup"><span data-stu-id="b9fc5-104">Add-ins can specify to Outlook that upon the occurrence of a specific event, certain actions should take place.</span></span> <span data-ttu-id="b9fc5-105">Este mecanismo de alerta e callback é suportado por representantes do .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="b9fc5-105">This alert and callback mechanism is supported by delegates of the .NET Framework.</span></span> <span data-ttu-id="b9fc5-106"> Assembly de Interoperabilidade Primária do Outlook (PIA) define representantes aos quais você pode conectar métodos de callback para manipular eventos correspondentes.</span><span class="sxs-lookup"><span data-stu-id="b9fc5-106">The Outlook Primary Interop Assembly (PIA) defines delegates to which you can connect callback methods to handle corresponding events.</span></span> <span data-ttu-id="b9fc5-107">Este tópico descreve o processo de definir um método de callback e de conectá-lo como um manipulador de eventos para o objeto do Outlook.</span><span class="sxs-lookup"><span data-stu-id="b9fc5-107">This topic describes this process of defining a callback method and connecting it as an event handler to the Outlook object.</span></span>

## <a name="creating-a-callback-method"></a><span data-ttu-id="b9fc5-108">Criar um método de callback</span><span class="sxs-lookup"><span data-stu-id="b9fc5-108">Creating a Callback method</span></span>

<span data-ttu-id="b9fc5-109">Um callback é um método implementado para manipular a ocorrência de um evento específico, e é executado por uma fonte de notificação.</span><span class="sxs-lookup"><span data-stu-id="b9fc5-109">A callback is a method that is implemented to handle the occurrence of a specific event and is executed by a notification source.</span></span> <span data-ttu-id="b9fc5-110">No Outlook, os suplementos podem implementar métodos de callback para responder a certos eventos gerados pelo Outlook.</span><span class="sxs-lookup"><span data-stu-id="b9fc5-110">In Outlook, add-ins can implement callback methods to respond to certain events raised by Outlook.</span></span> <span data-ttu-id="b9fc5-111">O método de callback deve corresponder à assinatura do representante do evento.</span><span class="sxs-lookup"><span data-stu-id="b9fc5-111">This callback method must match the signature of the delegate of that event.</span></span> <span data-ttu-id="b9fc5-112">Por exemplo, para implementar um manipulador de eventos para o evento [ItemSend](https://msdn.microsoft.com/library/bb647198\(v=office.15\)), você precisa declarar o método de callback que corresponde à assinatura do representante correspondente:</span><span class="sxs-lookup"><span data-stu-id="b9fc5-112">For example, to implement an event handler for the [ItemSend](https://msdn.microsoft.com/library/bb647198\(v=office.15\)) event, you must declare the callback method that matches the signature of the corresponding delegate:</span></span>

```csharp
public delegate void ApplicationEvents_11_ItemSendEventHandler(object Item, ref bool Cancel)
```


```vb
Public Delegate Sub ApplicationEvents_11_ItemSendEventHandler(_
    ByVal Item As Object, ByRef Cancel As Boolean)
```

<span data-ttu-id="b9fc5-113">Ao definir o método de callback, ignore a palavra-chace **Delegate** que, do contrário, definiria outro representante.</span><span class="sxs-lookup"><span data-stu-id="b9fc5-113">When defining the callback method, ignore the **Delegate** keyword which otherwise would define another delegate.</span></span> <span data-ttu-id="b9fc5-114">Uma amostra de método de callback, **MyItemSendEventHandler**, é mostrada abaixo:</span><span class="sxs-lookup"><span data-stu-id="b9fc5-114">A sample callback method, **MyItemSendEventHandler**, is shown below:</span></span>

```csharp
public void MyItemSendEventHandler(object Item, ref bool Cancel)
```


```vb
Public Sub MyItemSendEventHandler (_
    ByVal Item As Object, ByRef Cancel As Boolean)
…
End Sub
```

## <a name="connecting-a-callback-method"></a><span data-ttu-id="b9fc5-115">Conexão com um método de callback</span><span class="sxs-lookup"><span data-stu-id="b9fc5-115">Connecting a Callback method</span></span>

<span data-ttu-id="b9fc5-116">Após implementar um método de callback para um evento, você pode conectá-lo ao objeto do Outlook de modo que o Outlook saiba que deve chamar o método como um manipulador de eventos daquele evento.</span><span class="sxs-lookup"><span data-stu-id="b9fc5-116">After implementing a callback method for an event, you can connect it to the Outlook object so that Outlook knows to call the method as an event handler of that event.</span></span> <span data-ttu-id="b9fc5-117">Observe que um evento pode ser manipulado por mais de um manipulador de eventos, e é aqui que entram em jogo os representantes que atribuem a manipulação de eventos a manipuladores de eventos.</span><span class="sxs-lookup"><span data-stu-id="b9fc5-117">Note that an event can be handled by more than one event handler, and this is where delegates that assign event handling to event handlers come into play.</span></span>

<span data-ttu-id="b9fc5-118">Retomando o último exemplo de especificação de um manipulador de eventos para o evento **ItemSend** do objeto **Application**, para conectar **MyItemSendEventHandler** ao objeto **Application** em C\#, crie uma instância do objeto representante, passe **MyItemSendEventHandler** para o construtor do objeto representante e depois adicione este objeto representante ao evento **ItemSend** usando o operador +=:</span><span class="sxs-lookup"><span data-stu-id="b9fc5-118">Continuing with the last example of specifying a event handler for the **ItemSend** event of the **Application** object, to connect **MyItemSendEventHandler** to the **Application** object in C\#, create an instance of the delegate object, pass **MyItemSendEventHandler** to the constructor of the delegate object, and then add this delegate object to the **ItemSend** event using the += operator:</span></span>

```csharp
app.ItemSend += new ApplicationEvents_11_ItemSendEventHandler(MyItemSendEventHandler)
```

<span data-ttu-id="b9fc5-119">No Visual Basic, use instrução **AddHandler** para associar o evento **ItemSend** ao manipulador de eventos **MyItemSendEventHandler**:</span><span class="sxs-lookup"><span data-stu-id="b9fc5-119">In Visual Basic, you use the **AddHandler** statement to associate the **ItemSend** event with the **MyItemSendEventHandler** event handler:</span></span>

```vb
AddHandler app.ItemSend, AddressOf MyItemSendEventHandler
```

## <a name="see-also"></a><span data-ttu-id="b9fc5-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="b9fc5-120">See also</span></span>

- [<span data-ttu-id="b9fc5-121">Eventos no Outlook PIA</span><span class="sxs-lookup"><span data-stu-id="b9fc5-121">Events in the Outlook PIA</span></span>](events-in-the-outlook-pia.md)
- [<span data-ttu-id="b9fc5-122">Objetos no Outlook PIA</span><span class="sxs-lookup"><span data-stu-id="b9fc5-122">Objects in the Outlook PIA</span></span>](objects-in-the-outlook-pia.md)

