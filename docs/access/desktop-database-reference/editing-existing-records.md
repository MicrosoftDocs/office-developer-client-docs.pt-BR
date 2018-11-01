---
title: Editando registros existentes
TOCTitle: Editing Existing Records
ms:assetid: 86b961e0-e0a5-85a2-1138-7ab2e696ec11
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249585(v=office.15)
ms:contentKeyID: 48546089
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c500f89b0f16062e43ace45f55eab9a593d071a2
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25884230"
---
# <a name="editing-existing-records"></a><span data-ttu-id="c81dc-102">Editando registros existentes</span><span class="sxs-lookup"><span data-stu-id="c81dc-102">Editing Existing Records</span></span>


<span data-ttu-id="c81dc-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="c81dc-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c81dc-p101">Para editar registros existentes, vá para a linha que você deseja editar e altere a propriedade **Value** dos campos a serem alterados. Para obter mais informações sobre a propriedade **Value** do objeto **Field**, consulte o [Capítulo 3: Examinando dados](chapter-3-examining-data.md). Dependendo do tipo de cursor, você usará **Update** ou **UpdateBatch** para enviar alterações de volta para a fonte de dados. Para obter mais informações, consulte o [Capítulo 5: Atualizando e persistindo dados](chapter-5-updating-and-persisting-data.md).</span><span class="sxs-lookup"><span data-stu-id="c81dc-p101">To edit existing records, move to the row you want to edit and change the **Value** property of the fields you want to change. For more information about the **Field** object's **Value** property, see [Chapter 3: Examining Data](chapter-3-examining-data.md). Depending on your cursor type, you will use **Update** or **UpdateBatch** to send changes back to the data source. For more information, see [Chapter 5: Updating and Persisting Data](chapter-5-updating-and-persisting-data.md).</span></span>

<span data-ttu-id="c81dc-p102">Em geral, é mais eficiente usar um procedimento armazenado com um objeto de comando para realizar atualizações, bem como para executar outras operações, pois o procedimento armazenado não requer a criação de um cursor. Para obter mais informações sobre cursores, consulte o [Capítulo 8: Noções básicas sobre cursores e proteções](chapter-8-understanding-cursors-and-locks.md).</span><span class="sxs-lookup"><span data-stu-id="c81dc-p102">It is usually more efficient to use a stored procedure with a command object to perform updates, as well as to perform other operations, because a stored procedure does not require the creation of a cursor. For more information about cursors, see [Chapter 8: Understanding Cursors and Locks](chapter-8-understanding-cursors-and-locks.md).</span></span>

