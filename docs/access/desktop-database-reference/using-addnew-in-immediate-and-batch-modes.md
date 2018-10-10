---
title: Usando AddNew nos Modos de atualização imediata e em lotes
TOCTitle: Using AddNew in Immediate and Batch Modes
ms:assetid: 1dc32284-9514-083d-ce56-58abbafa7bb7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248970(v=office.15)
ms:contentKeyID: 48543602
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b37acc1819d12acc1e659be85361c3c09b84ebdb
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462998"
---
# <a name="using-addnew-in-immediate-and-batch-modes"></a>Usando AddNew nos Modos de atualização imediata e em lotes


**Aplica-se a**: Access 2013 | Office 2013

O comportamento do método **AddNew** depende do modo de atualização do objeto **Recordset** e se serão passados os argumentos *FieldList* e *Values* .

No modo de atualização imediata (em que o provedor grava as alterações na fonte de dados subjacente quando você chama o método **Update**), a chamada do método **AddNew** sem argumentos define a propriedade **EditMode** como **adEditAdd.** O provedor armazena no cache local as alterações de valores de campo. A chamada do método **Update** posta o novo registro no banco de dados e redefine a propriedade **EditMode** como **adEditNone**. Se você passar os argumentos *FieldList* e *Values*, o ADO postará imediatamente o novo registro no banco de dados (não será necessário chamar **Update**); o valor da propriedade **EditMode** não será alterado (**adEditNone**).

No modo de atualização em lotes, a chamada do método **AddNew** sem argumentos define a propriedade **EditMode** como **adEditAdd**. O provedor armazena no cache local as alterações de valores de campo. A chamada do método **Update** adiciona o novo registro ao **Recordset** atual e redefine a propriedade **EditMode** em **adEditNone**, mas o provedor não posta as alterações no banco de dados subjacente até a chamada do método **UpdateBatch**. Se você passar os argumentos *FieldList* e *Values* , ADO envia o novo registro para o provedor de armazenamento em cache; Você precisará chamar o método **UpdateBatch** para lançar o novo registro no banco de dados subjacente. Para obter mais informações sobre os métodos **Update** e **UpdateBatch**, consulte o [Capítulo 5: Atualizando e persistindo dados](chapter-5-updating-and-persisting-data.md).

