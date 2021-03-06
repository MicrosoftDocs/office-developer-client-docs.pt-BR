---
title: Como os manipuladores de eventos funcionam juntos
TOCTitle: How event handlers work together
ms:assetid: 02122824-881e-0bb8-cba1-c963024790ae
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248788(v=office.15)
ms:contentKeyID: 48542951
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e772e93f27d6bb5f30d865e3435d4bde6bdc5e73
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291919"
---
# <a name="how-event-handlers-work-together"></a>Como os manipuladores de eventos funcionam juntos

**Aplica-se ao:** Access 2013, Office 2013

A menos que esteja fazendo uma programação em Visual Basic, todos os manipuladores de eventos **Connection** e **Recordset** deverão ser implementados, independentemente do processamento ou não de todos os eventos. O volume de implementação a ser executado dependerá da linguagem de programação. Para obter mais informações, consulte [Instanciação de eventos ADO por linguagem](https://docs.microsoft.com/office/client-developer/access/desktop-database-reference/ado-event-instantiation-by-language-ado).

## <a name="paired-event-handlers"></a>Manipuladores de eventos emparelhados

Each Will event handler has an associated Complete event handler. For example, when your application changes the value of a field, the **WillChangeField** event handler is called. If the change is acceptable, your application leaves the **adStatus** parameter unchanged and the operation is performed. When the operation completes, a **FieldChangeComplete** event notifies your application that the operation has finished. If it completed successfully, **adStatus** contains **adStatusOK**; otherwise, **adStatus** contains **adStatusErrorsOccurred** and you must check the **Error** object to determine the cause of the error.

Quando **WillChangeField** for chamado, você poderá determinar a não execução da alteração. Nesse caso, defina **adStatus** como **adStatusCancel**. A operação será cancelada e o evento **FieldChangeComplete** receberá o valor **adStatusErrorsOccurred** para **adStatus**. O objeto **Error** contém **adErrOperationCancelled**, para que o manipulador **FieldChangeComplete** saiba sobre o cancelamento da operação. Entretanto, você precisará verificar o valor do parâmetro **adStatus** antes de alterá-lo já que a configuração de **adStatus** como **adStatusCancel** não terá efeito se o parâmetro tiver sido definido como **adStatusCantDeny** na entrada para o procedimento.

Algumas vezes, uma operação pode gerar mais de um evento. Por exemplo, o objeto **Recordset** possui eventos associados para alterações de **Field** e para alterações de **Record**. Quando seu aplicativo alterar o valor de um **Field**, o manipulador de eventos **WillChangeField** será chamado. Se ele determinar que é possível continuar a operação, o manipulador de eventos **WillChangeRecord** também será gerado. Se esse manipulador também permitir a continuação do evento, a alteração será efetuada e os manipuladores de eventos **FieldChangeComplete** e **RecordChangeComplete** serão chamados. A ordem de chamada dos manipuladores de eventos Will para uma operação específica é indefinida, portanto, evite criar um código que dependa da chamada de manipuladores em uma sequência específica.

Em instâncias com vários eventos Will gerados, um dos eventos poderá cancelar a operação pendente. Por exemplo, quando seu aplicativo altera o valor de um **Field**, normalmente os manipuladores de eventos **WillChangeField** e **WillChangeRecord** são chamados. Entretanto, se a operação for cancelada no primeiro manipulador de eventos, seu manipulador Complete associado será imediatamente chamado através de **adStatusOperationCancelled**. O segundo manipulador nunca é chamado. No entanto, se o primeiro manipulador de eventos permitir a continuação do evento, o outro será chamado. Se, em seguida, ele cancelar a operação, os dois eventos Complete serão chamados como nos exemplos anteriores.

## <a name="unpaired-event-handlers"></a>Manipuladores de eventos não formados

Caso o status passado para o evento seja diferente de **adStatusCantDeny**, você poderá desativar as notificações para qualquer evento, retornando **adStatusUnwantedEvent** no parâmetro *Status*. Por exemplo, quando o manipulador de eventos Complete for chamado pela primeira vez, você poderá retornar  **adStatusUnwantedEvent**. Em seguida, você receberá apenas eventos Will. Entretanto, alguns eventos podem ser disparados por mais de um motivo. Nesse caso, o evento terá um parâmetro *Reason*. Ao retornar **adStatusUnwantedEvent**, você não receberá mais notificações desse evento, somente quando elas ocorrerem por um motivo específico. Isso significa que você provavelmente receberá uma notificação de cada possível motivo para o disparo do evento.

Um único manipulador de eventos Will pode ser útil quando você deseja examinar os parâmetros a serem usados em uma operação. Você pode modificar esses parâmetros de operação ou cancelar a operação.

Você também pode manter a notificação do evento Complete habilitada. Quando o primeiro manipulador de eventos Will for chamado, retorne **adStatusUnwantedEvent**. Em seguida, você receberá apenas eventos Complete.

Um único manipulador de eventos Complete pode ser útil para o gerenciamento de operações assíncronas. Cada operação assíncrona possui um evento Complete apropriado.

Por exemplo, o preenchimento de um grande objeto [Recordset](recordset-object-ado.md) pode ser demorado. Se o aplicativo for escrito adequadamente, você poderá iniciar uma operação e continuar com outros processamentos. No final, você será notificado quando **Recordset** for preenchido por um evento **ExecuteComplete**.

## <a name="single-event-handlers-and-multiple-objects"></a>Manipuladores de eventos individuais e vários objetos

A flexibilidade de uma linguagem de programação como o Microsoft Visual C++ permite ter eventos de processo de um único manipulador de eventos a partir de vários objetos. Por exemplo, você pode ter eventos de processo de um único manipulador de eventos **Disconnect** a partir de vários objetos **Connection**. Se uma das conexões for encerrada, o manipulador de eventos **Disconnect** será chamado. É possível saber qual conexão causou o evento, pois o parâmetro de objeto manipulador de eventos é definido para o objeto **Connection** correspondente.

> [!NOTE]
> [!OBSERVAçãO] Essa técnica não pode ser usada no Visual Basic, pois essa linguagem apenas pode correlacionar um objeto a um manipulador de eventos.


