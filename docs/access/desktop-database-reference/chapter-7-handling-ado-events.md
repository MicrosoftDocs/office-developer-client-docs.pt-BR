---
title: 'Capítulo 7: Controlando eventos ADO'
TOCTitle: 'Chapter 7: Handling ADO Events'
ms:assetid: 22924fe2-d00d-8a0c-52f5-2dc6039537ff
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249004(v=office.15)
ms:contentKeyID: 48543709
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 816dd98e5e4c21f3159edf18b5687b2b0578e399
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25860837"
---
# <a name="chapter-7-handling-ado-events"></a>Capítulo 7: Controlando eventos ADO


**Aplica-se a**: Access 2013 | Office 2013

O modelo de evento ADO oferece suporte a determinadas operações ADO síncronas e assíncronas que emitem *eventos*, ou notificações, antes de a operação começar ou depois de ela ser concluída. Um evento geralmente é uma chamada a uma rotina do manipulador de eventos que você define no aplicativo.

Se você fornecer funções ou procedimentos do manipulador para o grupo de eventos que ocorrem antes de a operação começar, poderá examinar ou modificar os parâmetros transmitidos para a operação. Uma vez que ainda não foi executada, você poderá cancelar a operação ou permitir que ela seja concluída.

O grupo de eventos que ocorrem depois de uma operação concluir são especificamente importantes se você usar o ADO de maneira assíncrona. Por exemplo, um aplicativo que inicia uma operação [Recordset.Open](open-method-ado-recordset.md) assíncrona é notificado por um evento de conclusão de execução quando a operação for concluída.

O uso do modelo de eventos ADO adiciona uma sobrecarga no aplicativo, mas oferece muito mais flexibilidade do que os outros métodos de lidar com operações assíncronas, como o monitoramento da propriedade [State](state-property-ado.md) de um objeto com um loop.

Este capítulo aborda os seguintes tópicos:

- [Resumo do manipulador de eventos ADO](ado-event-handler-summary.md)

- [Tipos de eventos](types-of-events.md)

- [Parâmetros de eventos](event-parameters.md)

- [Como os manipuladores de eventos funcionam juntos](how-event-handlers-work-together.md)

- [Instanciação de eventos do ADO por linguagem (ADO)](ado-event-instantiation-by-language-ado.md)