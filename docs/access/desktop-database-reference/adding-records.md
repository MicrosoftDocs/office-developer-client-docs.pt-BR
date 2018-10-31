---
title: Adicionando registros (referência de banco de dados da área de trabalho do Access)
TOCTitle: Adding Records
ms:assetid: 7a5b27bc-7b28-4f43-b55e-a21edfb9e1b3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249505(v=office.15)
ms:contentKeyID: 48545791
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f235d7535f15eea7bd5d4c2abb88abb1a30935c7
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25862498"
---
# <a name="adding-records"></a><span data-ttu-id="57c70-102">Adição de registros</span><span class="sxs-lookup"><span data-stu-id="57c70-102">Adding Records</span></span>


<span data-ttu-id="57c70-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="57c70-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="57c70-p101">Use o método **AddNew** para criar e inicializar um novo registro em um **Recordset**. Você pode usar o método **Supports** com o valor **CursorOptionEnum** **adAddNew** para verificar se é possível adicionar registros ao objeto **Recordset** atual.</span><span class="sxs-lookup"><span data-stu-id="57c70-p101">Use the **AddNew** method to create and initialize a new record in an existing **Recordset**. You can use the **Supports** method with a **CursorOptionEnum** value of **adAddNew** to verify whether you can add records to the current **Recordset** object.</span></span>

<span data-ttu-id="57c70-p102">Depois que você chamar o método **AddNew**, o novo registro se tornará o registro atual e permanecerá atual até a chamada do método **Update**. Se o objeto **Recordset** não oferecer suporte a indicadores, pode ser que você não consiga acessar o novo registro se passar para outro. Assim, dependendo do tipo de cursor, talvez seja necessário chamar o método **Requery** para tornar o novo registro acessível.</span><span class="sxs-lookup"><span data-stu-id="57c70-p102">After you call the **AddNew** method, the new record becomes the current record and remains current after you call the **Update** method. If the **Recordset** object does not support bookmarks, you might not be able to access the new record once you move to another record. Therefore, depending on your cursor type, you might need to call the **Requery** method to make the new record accessible.</span></span>

<span data-ttu-id="57c70-109">Se você chamar **AddNew** durante a edição do registro atual ou a adição de um novo registro, o ADO chamará o método **Update** para salvar as alterações e, em seguida, criará o novo registro.</span><span class="sxs-lookup"><span data-stu-id="57c70-109">If you call **AddNew** while editing the current record or while adding a new record, ADO calls the **Update** method to save any changes and then creates the new record.</span></span>

<span data-ttu-id="57c70-110">Esta seção inclui os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="57c70-110">This section includes the following topics:</span></span>

- [<span data-ttu-id="57c70-111">Adição de vários campos</span><span class="sxs-lookup"><span data-stu-id="57c70-111">Adding Multiple Fields</span></span>](adding-multiple-fields.md)

- [<span data-ttu-id="57c70-112">Determinação do modo de edição</span><span class="sxs-lookup"><span data-stu-id="57c70-112">Determining Edit Mode</span></span>](determining-edit-mode.md)

- [<span data-ttu-id="57c70-113">Usando AddNew nos Modos de atualização imediata e em lotes</span><span class="sxs-lookup"><span data-stu-id="57c70-113">Using AddNew in Immediate and Batch Modes</span></span>](using-addnew-in-immediate-and-batch-modes.md)

