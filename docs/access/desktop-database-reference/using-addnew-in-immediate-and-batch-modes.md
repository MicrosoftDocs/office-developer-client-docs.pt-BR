---
title: Usando AddNew nos Modos de atualização imediata e em lotes
TOCTitle: Using AddNew in Immediate and Batch Modes
ms:assetid: 1dc32284-9514-083d-ce56-58abbafa7bb7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248970(v=office.15)
ms:contentKeyID: 48543602
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 79bd4ed656da49e61ea70ace3b11f09c19382b03
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25943637"
---
# <a name="using-addnew-in-immediate-and-batch-modes"></a><span data-ttu-id="86cf6-102">Usando AddNew nos modos Immediate e em lotes</span><span class="sxs-lookup"><span data-stu-id="86cf6-102">Using AddNew in Immediate and Batch modes</span></span>


<span data-ttu-id="86cf6-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="86cf6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="86cf6-104">O comportamento do método **AddNew** depende do modo de atualização do objeto **Recordset** e se serão passados os argumentos *FieldList* e *Values* .</span><span class="sxs-lookup"><span data-stu-id="86cf6-104">The behavior of the **AddNew** method depends on the updating mode of the **Recordset** object and whether you pass the *FieldList* and *Values* arguments.</span></span>

<span data-ttu-id="86cf6-p101">No modo de atualização imediata (em que o provedor grava as alterações na fonte de dados subjacente quando você chama o método **Update**), a chamada do método **AddNew** sem argumentos define a propriedade **EditMode** como **adEditAdd.** O provedor armazena no cache local as alterações de valores de campo. A chamada do método **Update** posta o novo registro no banco de dados e redefine a propriedade **EditMode** como **adEditNone**. Se você passar os argumentos *FieldList* e *Values*, o ADO postará imediatamente o novo registro no banco de dados (não será necessário chamar **Update**); o valor da propriedade **EditMode** não será alterado (**adEditNone**).</span><span class="sxs-lookup"><span data-stu-id="86cf6-p101">In immediate update mode (in which the provider writes changes to the underlying data source once you call the **Update** method), calling the **AddNew** method without arguments sets the **EditMode** property to **adEditAdd.** The provider caches any field value changes locally. Calling the **Update** method posts the new record to the database and resets the **EditMode** property to **adEditNone**. If you pass the *FieldList* and *Values* arguments, ADO immediately posts the new record to the database (no **Update** call is necessary); the **EditMode** property value does not change (**adEditNone**).</span></span>

<span data-ttu-id="86cf6-109">No modo de atualização em lotes, a chamada do método **AddNew** sem argumentos define a propriedade **EditMode** como **adEditAdd**.</span><span class="sxs-lookup"><span data-stu-id="86cf6-109">In batch update mode, calling the **AddNew** method without arguments sets the **EditMode** property to **adEditAdd**.</span></span> <span data-ttu-id="86cf6-110">O provedor armazena no cache local as alterações de valores de campo.</span><span class="sxs-lookup"><span data-stu-id="86cf6-110">The provider caches any field value changes locally.</span></span> <span data-ttu-id="86cf6-111">A chamada do método **Update** adiciona o novo registro ao **Recordset** atual e redefine a propriedade **EditMode** em **adEditNone**, mas o provedor não posta as alterações no banco de dados subjacente até a chamada do método **UpdateBatch**.</span><span class="sxs-lookup"><span data-stu-id="86cf6-111">Calling the **Update** method adds the new record to the current **Recordset** and resets the **EditMode** property to **adEditNone**, but the provider does not post the changes to the underlying database until you call the **UpdateBatch** method.</span></span> <span data-ttu-id="86cf6-112">Se você passar os argumentos *FieldList* e *Values* , ADO envia o novo registro para o provedor de armazenamento em cache; Você precisará chamar o método **UpdateBatch** para lançar o novo registro no banco de dados subjacente.</span><span class="sxs-lookup"><span data-stu-id="86cf6-112">If you pass the *FieldList* and *Values* arguments, ADO sends the new record to the provider for storage in a cache; you need to call the **UpdateBatch** method to post the new record to the underlying database.</span></span> <span data-ttu-id="86cf6-113">Para obter mais informações sobre os métodos **Update** e **UpdateBatch**, consulte o [Capítulo 5: Atualizando e persistindo dados](chapter-5-updating-and-persisting-data.md).</span><span class="sxs-lookup"><span data-stu-id="86cf6-113">For more information about **Update** and **UpdateBatch**, see [Chapter 5: Updating and Persisting Data](chapter-5-updating-and-persisting-data.md).</span></span>

