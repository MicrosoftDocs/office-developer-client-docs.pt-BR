---
title: Propriedades Unique Table, Unique Schema, Unique Catalog -- Dinâmicas (ADO)
TOCTitle: Unique Table, Unique Schema, Unique Catalog Properties--Dynamic (ADO)
ms:assetid: e6374782-755b-322b-21de-6d6a386dcd98
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250169(v=office.15)
ms:contentKeyID: 48548374
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 71701d605a9a9b156de7b2c6a23100e30932aaea
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25602087"
---
# <a name="unique-table-unique-schema-unique-catalog-properties--dynamic-ado"></a><span data-ttu-id="53938-102">Propriedades Unique Table, Unique Schema, Unique Catalog -- Dinâmicas (ADO)</span><span class="sxs-lookup"><span data-stu-id="53938-102">Unique Table, Unique Schema, Unique Catalog Properties--Dynamic (ADO)</span></span>


<span data-ttu-id="53938-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="53938-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="53938-104">Permite que você controle de perto as modificações em um determinada tabela base de um [Recordset](recordset-object-ado.md) formado por uma operação JOIN em diversas tabelas base.</span><span class="sxs-lookup"><span data-stu-id="53938-104">Enables you to closely control modifications to a particular base table in a [Recordset](recordset-object-ado.md) that was formed by a JOIN operation on multiple base tables.</span></span>

  - <span data-ttu-id="53938-105">**Unique Table** especifica o nome da tabela base na qual atualizações, inserções e exclusões são permitidas.</span><span class="sxs-lookup"><span data-stu-id="53938-105">**Unique Table** specifies the name of the base table upon which updates, insertions, and deletions are allowed.</span></span>

  - <span data-ttu-id="53938-106">**Unique Schema** especifica o *esquema* ou o nome do proprietário da tabela.</span><span class="sxs-lookup"><span data-stu-id="53938-106">**Unique Schema** specifies the *schema*, or name of the owner of the table.</span></span>

  - <span data-ttu-id="53938-107">**Unique Catalog** especifica o *catálogo* ou o nome do banco de dados que contém a tabela.</span><span class="sxs-lookup"><span data-stu-id="53938-107">**Unique Catalog** specifies the *catalog*, or name of the database containing the table.</span></span>

<span data-ttu-id="53938-108"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="53938-108"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="53938-109">Configurações e valor de retorno</span><span class="sxs-lookup"><span data-stu-id="53938-109">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="53938-110">Configurações e valores de retorno</span><span class="sxs-lookup"><span data-stu-id="53938-110">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="53938-111">mestre</span><span class="sxs-lookup"><span data-stu-id="53938-111">master</span></span>

<span data-ttu-id="53938-112">Define ou retorna um valor **String** que é o nome de uma tabela, um esquema ou um catálogo.</span><span class="sxs-lookup"><span data-stu-id="53938-112">Sets or returns a **String** value that is the name of a table, schema, or catalog.</span></span>

## <a name="remarks"></a><span data-ttu-id="53938-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="53938-113">Remarks</span></span>

<span data-ttu-id="53938-p101">A tabela base desejada é identificada com exclusividade por seus nomes de catálogo, esquema e tabela. Quando a propriedade **Unique Table** está definida, os valores das propriedades **Unique Schema** ou **Unique Catalog** são usados para localizar a tabela base. Deseja-se, mas não é necessário, que uma das propriedades **Unique Schema** e **Unique Catalog**, ou ambas, seja definida antes da propriedade **Unique Table**.</span><span class="sxs-lookup"><span data-stu-id="53938-p101">The desired base table is uniquely identified by its catalog, schema, and table names. When the **Unique Table** property is set, the values of the **Unique Schema** or **Unique Catalog** properties are used to find the base table. It is intended, but not required, that either or both the **Unique Schema** and **Unique Catalog** properties be set before the **Unique Table** property is set.</span></span>

<span data-ttu-id="53938-p102">A chave primária de **Unique Table** é tratada como a chave primária de todo o **Recordset**. Essa é a chave que será usada para qualquer método que exija uma chave primária.</span><span class="sxs-lookup"><span data-stu-id="53938-p102">The primary key of the **Unique Table** is treated as the primary key of the entire **Recordset**. This is the key that is used for any method requiring a primary key.</span></span>

<span data-ttu-id="53938-p103">Enquanto **Unique Table** estiver definida, o método [Delete](delete-method-ado-recordset.md) afetará apenas a tabela nomeada. Os métodos [AddNew](addnew-method-ado.md), [Resync](resync-method-ado.md), [Update](update-method-ado.md) e [UpdateBatch](updatebatch-method-ado.md) afetam quaisquer tabelas base subjacentes do **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="53938-p103">While **Unique Table** is set, the [Delete](delete-method-ado-recordset.md) method affects only the named table. The [AddNew](addnew-method-ado.md), [Resync](resync-method-ado.md), [Update](update-method-ado.md), and [UpdateBatch](updatebatch-method-ado.md) methods affect any appropriate underlying base tables of the **Recordset**.</span></span>

<span data-ttu-id="53938-p104">A **Unique Table** deve ser especificada antes da realização de qualquer ressincronização personalizada. Se **Unique Table** não tiver sido especificada, a propriedade [Resync Command](resync-command-property-dynamic-ado.md) não terá efeito algum.</span><span class="sxs-lookup"><span data-stu-id="53938-p104">**Unique Table** must be specified before doing any custom resynchronizations. If **Unique Table** has not been specified, the [Resync Command](resync-command-property-dynamic-ado.md) property will have no effect.</span></span>

<span data-ttu-id="53938-123">Um erro em tempo de execução será o resultado se não for possível encontrar uma tabela base exclusiva.</span><span class="sxs-lookup"><span data-stu-id="53938-123">A run-time error results if a unique base table cannot be found.</span></span>

<span data-ttu-id="53938-124">Essas propriedades dinâmicas serão acrescentadas à coleção **Properties** do objeto [Recordset](properties-collection-ado.md) quando a propriedade [CursorLocation](cursorlocation-property-ado.md) for definida como **adUseClient**.</span><span class="sxs-lookup"><span data-stu-id="53938-124">These dynamic properties are all appended to the **Recordset** object [Properties](properties-collection-ado.md) collection when the [CursorLocation](cursorlocation-property-ado.md) property is set to **adUseClient**.</span></span>

