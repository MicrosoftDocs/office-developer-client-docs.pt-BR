---
title: Coleção Fields (ADO)
TOCTitle: Fields collection (ADO)
ms:assetid: 029aa738-8726-54a6-1813-b152813948bc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248791(v=office.15)
ms:contentKeyID: 48542962
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a537756483361733c087d5dc1c6bba6e649d17d6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292570"
---
# <a name="fields-collection-ado"></a><span data-ttu-id="338b4-102">Coleção Fields (ADO)</span><span class="sxs-lookup"><span data-stu-id="338b4-102">Fields collection (ADO)</span></span>


<span data-ttu-id="338b4-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="338b4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="338b4-104">Contém todos os objetos [Field](field-object-ado.md) de um objeto [Recordset](recordset-object-ado.md) ou [Record](record-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="338b4-104">Contains all the [Field](field-object-ado.md) objects of a [Recordset](recordset-object-ado.md) or [Record](record-object-ado.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="338b4-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="338b4-105">Remarks</span></span>

<span data-ttu-id="338b4-p101">Um objeto **Recordset** tem uma coleção **Fields** composta de objetos **Field**. Cada objeto **Field** corresponde a uma coluna do **Recordset**. Preencha a coleção **Fields** antes de abrir o **Recordset** chamando o método [Refresh](refresh-method-ado.md) da coleção.</span><span class="sxs-lookup"><span data-stu-id="338b4-p101">A **Recordset** object has a **Fields** collection made up of **Field** objects. Each **Field** object corresponds to a column in the **Recordset**. You can populate the **Fields** collection before opening the **Recordset** by calling the [Refresh](refresh-method-ado.md) method on the collection.</span></span>

> [!NOTE]
> <span data-ttu-id="338b4-109">[!OBSERVAçãO] Consulte o tópico do objeto **Field** para obter uma explicação detalhada sobre como usar os objetos **Field**.</span><span class="sxs-lookup"><span data-stu-id="338b4-109">See the **Field** object topic for a more detailed explanation of how to use **Field** objects.</span></span>

<span data-ttu-id="338b4-110">A coleção **Fields** tem um método [Append](append-method-ado.md), que cria e adiciona, de forma provisória, um objeto **Field** a uma coleção, e um método **Update**, que finaliza qualquer adição ou exclusão.</span><span class="sxs-lookup"><span data-stu-id="338b4-110">The **Fields** collection has an [Append](append-method-ado.md) method, which provisionally creates and adds a **Field** object to the collection, and an **Update** method, which finalizes any additions or deletions.</span></span>

<span data-ttu-id="338b4-p102">Um objeto **Record** que tem dois campos especiais que podem ser indexados com constantes [FieldEnum](fieldenum.md). Uma constante acessa um campo que contém o fluxo padrão do **Record** e a outra que acessa um campo que contém uma sequência URL absoluta para o **Record**.</span><span class="sxs-lookup"><span data-stu-id="338b4-p102">A **Record** object has two special fields that can be indexed with [FieldEnum](fieldenum.md) constants. One constant accesses a field containing the default stream for the **Record**, and the other accesses a field containing the absolute URL string for the **Record**.</span></span>

<span data-ttu-id="338b4-p103">Determinados provedores (por exemplo, o [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md)) podem preencher a coleção **Fields** com um subconjunto de campos disponíveis para o **Record** ou **Recordset**. Outros campos não serão adicionados à coleção até que sejam mencionados primeiro pelo nome ou indexados pelo código.</span><span class="sxs-lookup"><span data-stu-id="338b4-p103">Certain providers (for example, the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md)) may populate the **Fields** collection with a subset of available fields for the **Record** or **Recordset**. Other fields will not be added to the collection until they are first referenced by name or indexed by your code.</span></span>

<span data-ttu-id="338b4-p104">Caso você tente mencionar um campo não existente pelo nome, um novo objeto **Field** será anexado à coleção **Fields** com um [Status](status-property-ado-field.md) de **adFieldPendingInsert**. Quando você chamar [Update](update-method-ado.md), o ADO criará um novo campo na fonte de dados, se permitido pelo provedor.</span><span class="sxs-lookup"><span data-stu-id="338b4-p104">If you attempt to reference a nonexistent field by name, a new **Field** object will be appended to the **Fields** collection with a [Status](status-property-ado-field.md) of **adFieldPendingInsert**. When you call [Update](update-method-ado.md), ADO will create a new field in your data source if allowed by your provider.</span></span>

