---
title: Alternância para um registro
TOCTitle: Jumping to a record
ms:assetid: 27177bbe-066c-aeb0-6dfd-45d8c2a87487
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249033(v=office.15)
ms:contentKeyID: 48543829
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 08d8a3d7b3d6012867a91aa306f45872bfebb2e1
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28714476"
---
# <a name="jumping-to-a-record"></a>Alternância para um registro


**Aplica-se a**: Access 2013, o Office 2013

O método [Move](move-method-ado.md) permite que você avance ou retroceda um número específico de registros no **Recordset** usando a seguinte sintaxe:

```vb 
 
oRs.Move NumRecords, Start
```

Há suporte no método **Move** para todos os objetos **Recordset**.

Se o argumento *NumRecords* for maior que zero, a posição de registro atual é movida para frente (em direção ao final do **Recordset**). Se *NumRecords* for menor que zero, a posição de registro atual será movida para trás (em direção ao início do **Recordset**).

Se a chamada de **Move** mover a posição de registro atual para um ponto antes do primeiro registro, o ADO define o registro atual para a posição antes do primeiro registro no **Recordset** (**BOF** é **True**). Uma tentativa em mover para trás quando a propriedade **BOF** já é **True** gera um erro.

Se a chamada de **Move** mover a posição do registro atual para um ponto depois do último registro, o ADO define o registro atual para a posição depois do último registro no **Recordset** (**EOF** é **True**). Uma tentativa em mover para frente quando a propriedade **EOF** já é **True** gera um erro.

Chamar o método **Move** a partir de um objeto **Recordset** vazio gera um erro.

Se você passar um indicador no argumento *Start* , a movimentação é relativo record com este indicador, supondo que o objeto **Recordset** suporta indicadores. Um indicador é obtido usando a propriedade [Bookmark](bookmark-property-ado.md). Se não for especificado, o movimento será relativo ao registro atual.

Força o ADO para recuperar um novo grupo de registros, se você estiver usando a propriedade **CacheSize** para registros no cache localmente do provedor, passando um argumento *NumRecords* que move a posição do registro atual fora do grupo atual de registros armazenados em cache Iniciando o registro de destino. A propriedade **CacheSize** determina o tamanho do grupo recém-recuperado e o registro de destino é o primeiro registro recuperado.

