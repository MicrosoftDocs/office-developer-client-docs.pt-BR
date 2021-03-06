---
title: Usando AddNew nos Modos de atualização imediata e em lotes
TOCTitle: Using AddNew in Immediate and Batch Modes
ms:assetid: 1dc32284-9514-083d-ce56-58abbafa7bb7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248970(v=office.15)
ms:contentKeyID: 48543602
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 929c01032924182d8db1bd5b06b573fb5d0171ae
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32312751"
---
# <a name="using-addnew-in-immediate-and-batch-modes"></a>Usando AddNew nos modos Imediato e Em Lotes


**Aplica-se ao:** Access 2013, Office 2013

O comportamento do método **AddNew** depende do modo de atualização do objeto **Recordset** e da passagem dos argumentos *FieldList* e *Values*.

No modo de atualização imediata (em que o provedor grava as alterações na fonte de dados subjacente quando você chama o método **Update**), a chamada do método **AddNew** sem argumentos define a propriedade **EditMode** como **adEditAdd.** O provedor armazena no cache local as alterações de valores de campo. A chamada do método **Update** posta o novo registro no banco de dados e redefine a propriedade **EditMode** como **adEditNone**. Se você passar os argumentos *FieldList* e *Values*, o ADO postará imediatamente o novo registro no banco de dados (não será necessário chamar **Update**); o valor da propriedade **EditMode** não será alterado (**adEditNone**).

No modo de atualização em lotes, a chamada do método **AddNew** sem argumentos define a propriedade **EditMode** como **adEditAdd**. O provedor armazena no cache local as alterações de valores de campo. A chamada do método **Update** adiciona o novo registro ao **Recordset** atual e redefine a propriedade **EditMode** em **adEditNone**, mas o provedor não posta as alterações no banco de dados subjacente até a chamada do método **UpdateBatch**. Se você passar os argumentos *FieldList* e *Values*, o ADO enviará o novo registro ao provedor para que seja armazenado em um cache; será necessário chamar o método **UpdateBatch** para postar o novo registro no banco de dados subjacente. Para obter mais informações sobre os métodos **Update** e **UpdateBatch**, consulte o [Capítulo 5: Atualizando e persistindo dados](chapter-5-updating-and-persisting-data.md).

