---
title: Adicionando registros (referência de banco de dados da área de trabalho do Access)
TOCTitle: Adding records
ms:assetid: 7a5b27bc-7b28-4f43-b55e-a21edfb9e1b3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249505(v=office.15)
ms:contentKeyID: 48545791
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 177eeb0499f3ba3376237c4773e776f8c7c7583f
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25946507"
---
# <a name="adding-records"></a><span data-ttu-id="f7ad2-102">Adicionando registros</span><span class="sxs-lookup"><span data-stu-id="f7ad2-102">Adding records</span></span>

<span data-ttu-id="f7ad2-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="f7ad2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f7ad2-p101">Use o método **AddNew** para criar e inicializar um novo registro em um **Recordset**. Você pode usar o método **Supports** com o valor **CursorOptionEnum** **adAddNew** para verificar se é possível adicionar registros ao objeto **Recordset** atual.</span><span class="sxs-lookup"><span data-stu-id="f7ad2-p101">Use the **AddNew** method to create and initialize a new record in an existing **Recordset**. You can use the **Supports** method with a **CursorOptionEnum** value of **adAddNew** to verify whether you can add records to the current **Recordset** object.</span></span>

<span data-ttu-id="f7ad2-p102">Depois que você chamar o método **AddNew**, o novo registro se tornará o registro atual e permanecerá atual até a chamada do método **Update**. Se o objeto **Recordset** não oferecer suporte a indicadores, pode ser que você não consiga acessar o novo registro se passar para outro. Assim, dependendo do tipo de cursor, talvez seja necessário chamar o método **Requery** para tornar o novo registro acessível.</span><span class="sxs-lookup"><span data-stu-id="f7ad2-p102">After you call the **AddNew** method, the new record becomes the current record and remains current after you call the **Update** method. If the **Recordset** object does not support bookmarks, you might not be able to access the new record once you move to another record. Therefore, depending on your cursor type, you might need to call the **Requery** method to make the new record accessible.</span></span>

<span data-ttu-id="f7ad2-109">Se você chamar **AddNew** durante a edição do registro atual ou a adição de um novo registro, o ADO chamará o método **Update** para salvar as alterações e, em seguida, criará o novo registro.</span><span class="sxs-lookup"><span data-stu-id="f7ad2-109">If you call **AddNew** while editing the current record or while adding a new record, ADO calls the **Update** method to save any changes and then creates the new record.</span></span>

<span data-ttu-id="f7ad2-110">Esta seção inclui os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="f7ad2-110">This section includes the following topics:</span></span>

- [<span data-ttu-id="f7ad2-111">Adicionando vários campos</span><span class="sxs-lookup"><span data-stu-id="f7ad2-111">Adding multiple fields</span></span>](adding-multiple-fields.md)
- [<span data-ttu-id="f7ad2-112">Determinando o modo de edição</span><span class="sxs-lookup"><span data-stu-id="f7ad2-112">Determining Edit mode</span></span>](determining-edit-mode.md)
- [<span data-ttu-id="f7ad2-113">Usando AddNew nos modos Immediate e em lotes</span><span class="sxs-lookup"><span data-stu-id="f7ad2-113">Using AddNew in Immediate and Batch modes</span></span>](using-addnew-in-immediate-and-batch-modes.md)

