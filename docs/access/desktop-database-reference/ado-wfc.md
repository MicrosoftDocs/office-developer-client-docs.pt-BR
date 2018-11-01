---
title: ADO para Windows Foundation Classes (ADO/WFC)
TOCTitle: ADO/WFC
ms:assetid: 73206be8-6515-79e4-e904-cc2d0d59411d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249468(v=office.15)
ms:contentKeyID: 48545628
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: da01d44e1e681a2de41741b11a9c412181c2fd9e
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25885077"
---
# <a name="adowfc"></a><span data-ttu-id="af902-102">ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="af902-102">ADO/WFC</span></span>


<span data-ttu-id="af902-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="af902-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="af902-p101">O ADO for Windows Foundation Classes (ADO/WFC) é criado com base no modelo de evento do ADO e apresenta uma interface de programação de aplicativo simplificada. O ADO/WFC intercepta eventos do ADO, consolida os parâmetros de evento em uma única classe de evento e, em seguida, chama o manipulador de eventos.</span><span class="sxs-lookup"><span data-stu-id="af902-p101">ADO for Windows Foundation Classes (ADO/WFC) builds on the ADO event model and presents a simplified application programming interface. In general, ADO/WFC intercepts ADO events, consolidates the event parameters into a single event class, and then calls your event handler.</span></span>

<span data-ttu-id="af902-106">**Para usar eventos do ADO no ADO/WFC**</span><span class="sxs-lookup"><span data-stu-id="af902-106">**To use ADO events in ADO/WFC**</span></span>

1.  <span data-ttu-id="af902-p102">Defina seu próprio manipulador de eventos para processar um evento. Por exemplo, se você quiser processar o evento **ConnectComplete** na família **ConnectionEvent**, poderá usar este código:</span><span class="sxs-lookup"><span data-stu-id="af902-p102">Define your own event handler to process an event. For example, if you wanted to process the **ConnectComplete** event in the **ConnectionEvent** family, you might use this code:</span></span>
    
    ```java 
     
    public void onConnectComplete(Object sender,ConnectionEvent e) 
    { 
        System.out.println("onConnectComplete:" + e); 
    } 
    ```

2.  <span data-ttu-id="af902-p103">Defina um objeto manipulador parar representar o manipulador de eventos. Esse objeto deve ter o tipo de dados **ConnectEventHandler** para um evento do tipo **ConnectionEvent**, ou o tipo de dados **RecordsetEventHandler** para um evento do tipo **RecordsetEvent**. Por exemplo, crie o seguinte código para o manipulador de eventos **ConnectComplete**:</span><span class="sxs-lookup"><span data-stu-id="af902-p103">Define a handler object to represent your event handler. The handler object should be of data type **ConnectEventHandler** for an event of type **ConnectionEvent**, or data type **RecordsetEventHandler** for an event of type **RecordsetEvent**. For example, code the following for your **ConnectComplete** event handler:</span></span>
    
    ```java
        ConnectionEventHandler handler =  
                new ConnectionEventHandler(this, "onConnectComplete"); 
    ```

    <span data-ttu-id="af902-p104">O primeiro argumento do construtor **ConnectionEventHandler** é uma referência à classe que contém o manipulador de eventos nomeado no segundo argumento. O compilador Microsoft Visual J++ também oferece suporte a uma sintaxe equivalente:</span><span class="sxs-lookup"><span data-stu-id="af902-p104">The first argument of the **ConnectionEventHandler** constructor is a reference to the class that contains the event handler named in the second argument. The Microsoft Visual J++ compiler also supports an equivalent syntax:</span></span>
    
    ```java 
     
        ConnectionEventHandler handler =  
            new ConnectionEventHandler(this, "onConnectComplete"); 
    ```
    
    ```java 
     
        ConnectionEventHandler handler =  
            new ConnectionEventHandler(this.onConnectComplete); 
    ```
    
    <span data-ttu-id="af902-p105">O primeiro argumento do construtor **ConnectionEventHandler** é uma referência à classe que contém o manipulador de eventos nomeado no segundo argumento. O compilador Microsoft Visual J++ também oferece suporte a uma sintaxe equivalente:</span><span class="sxs-lookup"><span data-stu-id="af902-p105">The first argument of the **ConnectionEventHandler** constructor is a reference to the class that contains the event handler named in the second argument. The Microsoft Visual J++ compiler also supports an equivalent syntax:</span></span>
    
    ```java 
     
        ConnectionEventHandler handler =  
            new ConnectionEventHandler(this.onConnectComplete); 
    ```
    
    <span data-ttu-id="af902-116">

O único argumento é uma referência à classe desejada (\*\*this\*\*) e ao método na classe (\*\*onConnectComplete**).
</span><span class="sxs-lookup"><span data-stu-id="af902-116">The single argument is a reference to the desired class (**this**) and method within the class (**onConnectComplete**).</span></span>

3.  <span data-ttu-id="af902-117">Adicione o manipulador de eventos a uma lista de manipuladores designados para processar determinado tipo de evento.</span><span class="sxs-lookup"><span data-stu-id="af902-117">Add your event handler to a list of handlers designated to process a particular type of event.</span></span> <span data-ttu-id="af902-118">Use o método com um nome como \**addOn \* \* \* EventName*(*manipulador*).</span><span class="sxs-lookup"><span data-stu-id="af902-118">Use the method with a name such as \**addOn\*\*\*EventName*(*handler*).</span></span>

4.  <span data-ttu-id="af902-p107">O ADO/WFC implementa internamente todos os manipuladores de eventos do ADO. Portanto, um evento causado por uma operação **Connection** ou **Recordset** é interceptado por um manipulador de eventos do ADO/WFC. O manipulador de eventos do ADO/WFC passa os parâmetros **ConnectionEvent** do ADO em uma instância da classe **ConnectionEvent** do ADO/WFC, ou os parâmetros **RecordsetEvent** do ADO em uma instância da classe **RecordsetEvent** do ADO/WFC. Essas classes do ADO/WFC consolidam os parâmetros de evento do ADO; isto é, cada uma delas contém um membro de dados para cada parâmetro exclusivo em todos os métodos **ConnectionEvent** ou **RecordsetEvent** do ADO.</span><span class="sxs-lookup"><span data-stu-id="af902-p107">ADO/WFC internally implements all the ADO event handlers. Therefore, an event caused by a **Connection** or **Recordset** operation is intercepted by an ADO/WFC event handler. The ADO/WFC event handler passes ADO **ConnectionEvent** parameters in an instance of the ADO/WFC **ConnectionEvent** class, or ADO **RecordsetEvent** parameters in an instance of the ADO/WFC **RecordsetEvent** class. These ADO/WFC classes consolidate the ADO event parameters; that is, each ADO/WFC class contains one data member for each unique parameter in all the ADO **ConnectionEvent** or **RecordsetEvent** methods.</span></span>

5.  <span data-ttu-id="af902-p108">Em seguida, o ADO/WFC chama o manipulador de eventos com o objeto de evento do ADO/WFC. Por exemplo, o manipulador **onConnectComplete** tem uma assinatura como esta:</span><span class="sxs-lookup"><span data-stu-id="af902-p108">ADO/WFC then calls your event handler with the ADO/WFC event object. For example, your **onConnectComplete** handler has a signature like this:</span></span>
    
    ```java 
     
        public void onConnectComplete(Object sender,ConnectionEvent e) 
    ```
    
    <span data-ttu-id="af902-125">O primeiro argumento é o tipo de objeto que enviou o evento ([Conexão](connection-object-ado.md) ou [Recordset](recordset-object-ado.md)) e o segundo argumento é o objeto event do ADO/WFC (**ConnectionEvent** ou **RecordsetEvent**).</span><span class="sxs-lookup"><span data-stu-id="af902-125">The first argument is the type of object that sent the event ([Connection](connection-object-ado.md) or [Recordset](recordset-object-ado.md)), and the second argument is the ADO/WFC event object (**ConnectionEvent** or **RecordsetEvent**).</span></span> <span data-ttu-id="af902-126">A assinatura do manipulador de eventos é mais simples que a de um evento do ADO.</span><span class="sxs-lookup"><span data-stu-id="af902-126">The signature of your event handler is simpler than an ADO event.</span></span> <span data-ttu-id="af902-127">Contudo, você deve conhecer o modelo de evento do ADO para saber quais parâmetros se aplicam a um evento e como responder.</span><span class="sxs-lookup"><span data-stu-id="af902-127">However, you must still understand the ADO event model to know what parameters apply to an event and how to respond.</span></span>

6.  <span data-ttu-id="af902-p110">Retorne do manipulador de eventos para o manipulador do ADO/WFC referente ao evento do ADO. O ADO/WFC copia os membros de dados de eventos do ADO/WFC pertinentes de volta para os parâmetros de evento do ADO e, em seguida, o manipulador de eventos do ADO retorna.</span><span class="sxs-lookup"><span data-stu-id="af902-p110">Return from your event handler to the ADO/WFC handler for the ADO event. ADO/WFC copies pertinent ADO/WFC event data members back to the ADO event parameters, and then the ADO event handler returns.</span></span>

7.  <span data-ttu-id="af902-130">Quando terminar o processamento, remova o manipulador da lista de manipuladores de eventos do ADO/WFC.</span><span class="sxs-lookup"><span data-stu-id="af902-130">When you are finished processing, remove your handler from the list of ADO/WFC event handlers.</span></span> <span data-ttu-id="af902-131">Use o método com um nome como \**removeOn \* \* \* EventName*(*manipulador*).</span><span class="sxs-lookup"><span data-stu-id="af902-131">Use the method with a name such as \**removeOn\*\*\*EventName*(*handler*).</span></span>

