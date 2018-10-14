---
title: Usar associação tardia ao depender de várias versões do Outlook
TOCTitle: Using late binding if depending on multiple versions of Outlook
ms:assetid: 4e5412a0-d0f8-4819-ba0f-f36ba885f8f6
ms:mtpsurl: https://msdn.microsoft.com/library/office/bb610234(v=office.15)
ms:contentKeyID: 55119791
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 866faab04e8fcac1d91b233f801f05c023ac2164
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25407069"
---
# <a name="using-late-binding-if-depending-on-multiple-versions-of-outlook"></a>Usar associação tardia ao depender de várias versões do Outlook

Suplementos do Outlook gerenciados que usam o Assembly de Interoperabilidade Primário (PIA) são compilados com informações de tipo fornecidas pelo PIA. Esta **associação inicial** do tipo de informações para métodos e propriedades permite ao compilador realizar verificações de tipo e sintaxe para garantir que o número e o tipo de parâmetros corretos sejam passados ao método ou propriedade, e que o valor fornecido é do tipo esperado. 

No entanto, a associação inicial tem a desvantagem de introduzir incompatibilidade entre versões se um método ou propriedade que o suplemento chama tiver uma declaração diferente em uma versão anterior. Por exemplo, adicionar novos métodos e propriedades ou modificar os membros existentes de um objeto pode alterar o layout binário do objeto e causar problemas com um suplemento gerenciado que usa as informações mais recentes do tipo para automatizar uma versão anterior do Outlook. 

Nesses casos, a **associação tardia** aguarda até que o tempo de execução associe as chamadas de método e propriedades a seus objetos. A associação tardia pode ajudar a evitar complicações de tipos que sejam diferentes em diferentes versões do Outlook, e são especialmente úteis ao escrever suplementos que dependem de várias versões do Outlook.

A associação tardia envolve uma chamada da interface [IDispatch](https://docs.microsoft.com/windows/desktop/api/oaidl/nn-oaidl-idispatch) implementada pelo Outlook. Para usar a associação tardia em Visual C\#, use o método [System.Type.InvokeMember](https://docs.microsoft.com/dotnet/api/system.type.invokemember?view=netframework-4.7.2). Esse método chama [IDispatch::GetIDsOfNames](https://docs.microsoft.com/windows/desktop/api/oaidl/nf-oaidl-idispatch-getidsofnames) e [IDispatch::Invoke](https://docs.microsoft.com/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke) para vincular a métodos e propriedades do Outlook. O método IDispatch::GetIDsOfNames permite ao Visual C\# interrogar um objeto sobre quais métodos e propriedades ele dá suporte, e que método IDispatch::Invoke permite Visual C\# para chamar esses métodos e propriedades. 

<!-- PAGES 404 
For more information about using late binding in C\#, see [KB 302902: Binding for Office Automation Servers with Visual C\# .NET](https://go.microsoft.com/fwlink/?linkid=88971). For more information about using late binding in Visual Basic, see [KB 304661: How to Use Visual Basic .NET for Binding for Office Automation Servers](https://go.microsoft.com/fwlink/?linkid=88972).

Note that late binding requires obtaining a DispID for every method or property, so late binding generally does not perform as well as early binding. For more information about how early binding compares with late binding, see [KB 245115: Using Early Binding and Late Binding in Automation](https://go.microsoft.com/fwlink/?linkid=88973). -->

## <a name="see-also"></a>Confira também

- [Introdução à interoperabilidade entre COM e .NET](introduction-to-interoperability-between-com-and-net.md)

