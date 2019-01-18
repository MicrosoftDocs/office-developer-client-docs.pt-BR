---
title: Unique Table, Unique Schema, propriedades dinâmicas do Unique Catalog (ADO)
TOCTitle: Unique Table, Unique Schema, Unique Catalog dynamic properties (ADO)
ms:assetid: e6374782-755b-322b-21de-6d6a386dcd98
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250169(v=office.15)
ms:contentKeyID: 48548374
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5f4bf93afc200edd88e89cf5d4e90435c2476942
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28721350"
---
# <a name="unique-table-unique-schema-unique-catalog-dynamic-properties-ado"></a><span data-ttu-id="5dfaf-102">Unique Table, Unique Schema, propriedades dinâmicas do Unique Catalog (ADO)</span><span class="sxs-lookup"><span data-stu-id="5dfaf-102">Unique Table, Unique Schema, Unique Catalog dynamic properties (ADO)</span></span>


<span data-ttu-id="5dfaf-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="5dfaf-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5dfaf-104">Permite que você controle de perto as modificações em um determinada tabela base de um [Recordset](recordset-object-ado.md) formado por uma operação JOIN em diversas tabelas base.</span><span class="sxs-lookup"><span data-stu-id="5dfaf-104">Enables you to closely control modifications to a particular base table in a [Recordset](recordset-object-ado.md) that was formed by a JOIN operation on multiple base tables.</span></span>

  - <span data-ttu-id="5dfaf-105">**Unique Table** especifica o nome da tabela base na qual atualizações, inserções e exclusões são permitidas.</span><span class="sxs-lookup"><span data-stu-id="5dfaf-105">**Unique Table** specifies the name of the base table upon which updates, insertions, and deletions are allowed.</span></span>

  - <span data-ttu-id="5dfaf-106">**Unique Schema** especifica o *esquema* ou o nome do proprietário da tabela.</span><span class="sxs-lookup"><span data-stu-id="5dfaf-106">**Unique Schema** specifies the *schema*, or name of the owner of the table.</span></span>

  - <span data-ttu-id="5dfaf-107">**Unique Catalog** especifica o *catálogo* ou o nome do banco de dados que contém a tabela.</span><span class="sxs-lookup"><span data-stu-id="5dfaf-107">**Unique Catalog** specifies the *catalog*, or name of the database containing the table.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="5dfaf-108">Configurações e valores de retorno</span><span class="sxs-lookup"><span data-stu-id="5dfaf-108">Settings and return values</span></span>

<span data-ttu-id="5dfaf-109">Define ou retorna um valor **String** que é o nome de uma tabela, um esquema ou um catálogo.</span><span class="sxs-lookup"><span data-stu-id="5dfaf-109">Sets or returns a **String** value that is the name of a table, schema, or catalog.</span></span>

## <a name="remarks"></a><span data-ttu-id="5dfaf-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="5dfaf-110">Remarks</span></span>

<span data-ttu-id="5dfaf-p101">A tabela base desejada é identificada com exclusividade por seus nomes de catálogo, esquema e tabela. Quando a propriedade **Unique Table** está definida, os valores das propriedades **Unique Schema** ou **Unique Catalog** são usados para localizar a tabela base. Deseja-se, mas não é necessário, que uma das propriedades **Unique Schema** e **Unique Catalog**, ou ambas, seja definida antes da propriedade **Unique Table**.</span><span class="sxs-lookup"><span data-stu-id="5dfaf-p101">The desired base table is uniquely identified by its catalog, schema, and table names. When the **Unique Table** property is set, the values of the **Unique Schema** or **Unique Catalog** properties are used to find the base table. It is intended, but not required, that either or both the **Unique Schema** and **Unique Catalog** properties be set before the **Unique Table** property is set.</span></span>

<span data-ttu-id="5dfaf-p102">A chave primária de **Unique Table** é tratada como a chave primária de todo o **Recordset**. Essa é a chave que será usada para qualquer método que exija uma chave primária.</span><span class="sxs-lookup"><span data-stu-id="5dfaf-p102">The primary key of the **Unique Table** is treated as the primary key of the entire **Recordset**. This is the key that is used for any method requiring a primary key.</span></span>

<span data-ttu-id="5dfaf-p103">Enquanto **Unique Table** estiver definida, o método [Delete](delete-method-ado-recordset.md) afetará apenas a tabela nomeada. Os métodos [AddNew](addnew-method-ado.md), [Resync](resync-method-ado.md), [Update](update-method-ado.md) e [UpdateBatch](updatebatch-method-ado.md) afetam quaisquer tabelas base subjacentes do **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="5dfaf-p103">While **Unique Table** is set, the [Delete](delete-method-ado-recordset.md) method affects only the named table. The [AddNew](addnew-method-ado.md), [Resync](resync-method-ado.md), [Update](update-method-ado.md), and [UpdateBatch](updatebatch-method-ado.md) methods affect any appropriate underlying base tables of the **Recordset**.</span></span>

<span data-ttu-id="5dfaf-p104">A **Unique Table** deve ser especificada antes da realização de qualquer ressincronização personalizada. Se **Unique Table** não tiver sido especificada, a propriedade [Resync Command](resync-command-property-dynamic-ado.md) não terá efeito algum.</span><span class="sxs-lookup"><span data-stu-id="5dfaf-p104">**Unique Table** must be specified before doing any custom resynchronizations. If **Unique Table** has not been specified, the [Resync Command](resync-command-property-dynamic-ado.md) property will have no effect.</span></span>

<span data-ttu-id="5dfaf-120">Um erro em tempo de execução será o resultado se não for possível encontrar uma tabela base exclusiva.</span><span class="sxs-lookup"><span data-stu-id="5dfaf-120">A run-time error results if a unique base table cannot be found.</span></span>

<span data-ttu-id="5dfaf-121">Essas propriedades dinâmicas serão acrescentadas à coleção **Properties** do objeto [Recordset](properties-collection-ado.md) quando a propriedade [CursorLocation](cursorlocation-property-ado.md) for definida como **adUseClient**.</span><span class="sxs-lookup"><span data-stu-id="5dfaf-121">These dynamic properties are all appended to the **Recordset** object [Properties](properties-collection-ado.md) collection when the [CursorLocation](cursorlocation-property-ado.md) property is set to **adUseClient**.</span></span>

