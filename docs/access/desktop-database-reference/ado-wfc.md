---
title: ADO for Windows Foundation Classes (ADO/WFC)
TOCTitle: ADO/WFC
ms:assetid: 73206be8-6515-79e4-e904-cc2d0d59411d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249468(v=office.15)
ms:contentKeyID: 48545628
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: df9def320274df0eb4636aa237deb566dd5725b7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281719"
---
# <a name="adowfc"></a>ADO/WFC


**Aplica-se ao:** Access 2013, Office 2013

O ADO for Windows Foundation Classes (ADO/WFC) é criado com base no modelo de evento do ADO e apresenta uma interface de programação de aplicativo simplificada. O ADO/WFC intercepta eventos do ADO, consolida os parâmetros de evento em uma única classe de evento e, em seguida, chama o manipulador de eventos.

**Para usar eventos do ADO no ADO/WFC**

1.  Defina seu próprio manipulador de eventos para processar um evento. Por exemplo, se você quiser processar o evento **ConnectComplete** na família **ConnectionEvent**, poderá usar este código:
    
    ```java 
     
    public void onConnectComplete(Object sender,ConnectionEvent e) 
    { 
        System.out.println("onConnectComplete:" + e); 
    } 
    ```

2.  Defina um objeto manipulador parar representar o manipulador de eventos. Esse objeto deve ter o tipo de dados **ConnectEventHandler** para um evento do tipo **ConnectionEvent**, ou o tipo de dados **RecordsetEventHandler** para um evento do tipo **RecordsetEvent**. Por exemplo, crie o seguinte código para o manipulador de eventos **ConnectComplete**:
    
    ```java
        ConnectionEventHandler handler =  
                new ConnectionEventHandler(this, "onConnectComplete"); 
    ```

    O primeiro argumento do construtor **ConnectionEventHandler** é uma referência à classe que contém o manipulador de eventos nomeado no segundo argumento. O compilador Microsoft Visual J++ também oferece suporte a uma sintaxe equivalente:
    
    ```java 
     
        ConnectionEventHandler handler =  
            new ConnectionEventHandler(this, "onConnectComplete"); 
    ```
    
    ```java 
     
        ConnectionEventHandler handler =  
            new ConnectionEventHandler(this.onConnectComplete); 
    ```
    
    O primeiro argumento do construtor **ConnectionEventHandler** é uma referência à classe que contém o manipulador de eventos nomeado no segundo argumento. O compilador Microsoft Visual J++ também oferece suporte a uma sintaxe equivalente:
    
    ```java 
     
        ConnectionEventHandler handler =  
            new ConnectionEventHandler(this.onConnectComplete); 
    ```
    
    O único argumento é uma referência à classe desejada (**this**) e ao método na classe (**onConnectComplete**).

3.  Adicione o manipulador de eventos a uma lista de manipuladores designados para processar determinado tipo de evento. Use o método com um nome como **addOn***EventName*(*manipulador*).

4.  O ADO/WFC implementa internamente todos os manipuladores de eventos do ADO. Portanto, um evento causado por uma operação **Connection** ou **Recordset** é interceptado por um manipulador de eventos do ADO/WFC. O manipulador de eventos do ADO/WFC passa os parâmetros **ConnectionEvent** do ADO em uma instância da classe **ConnectionEvent** do ADO/WFC, ou os parâmetros **RecordsetEvent** do ADO em uma instância da classe **RecordsetEvent** do ADO/WFC. Essas classes do ADO/WFC consolidam os parâmetros de evento do ADO; isto é, cada uma delas contém um membro de dados para cada parâmetro exclusivo em todos os métodos **ConnectionEvent** ou **RecordsetEvent** do ADO.

5.  Em seguida, o ADO/WFC chama o manipulador de eventos com o objeto de evento do ADO/WFC. Por exemplo, o manipulador **onConnectComplete** tem uma assinatura como esta:
    
    ```java 
     
        public void onConnectComplete(Object sender,ConnectionEvent e) 
    ```
    
    O primeiro argumento é o tipo de objeto que enviou o evento ([Connection](connection-object-ado.md) ou [Recordset](recordset-object-ado.md)), e o segundo argumento é o objeto de evento do ADO/WFC (**ConnectionEvent** ou **RecordsetEvent**). A assinatura do manipulador de eventos é mais simples que a de um evento do ADO. Contudo, você deve conhecer o modelo de evento do ADO para saber quais parâmetros se aplicam a um evento e como responder.

6.  Retorne do manipulador de eventos para o manipulador do ADO/WFC referente ao evento do ADO. O ADO/WFC copia os membros de dados de eventos do ADO/WFC pertinentes de volta para os parâmetros de evento do ADO e, em seguida, o manipulador de eventos do ADO retorna.

7.  Quando terminar o processamento, remova o manipulador da lista de manipuladores de eventos do ADO/WFC. Use o método com um nome como **removeOn***EventName*(*manipulador*).

