---
title: Remodelagem (referência da área de trabalho do banco de dados do Access)
TOCTitle: Reshaping
ms:assetid: 89c6a0d6-3bf4-36ae-26ec-d4e60f920490
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249605(v=office.15)
ms:contentKeyID: 48546174
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c820e82669789d7c3806cc1fd38a2eb6844b722e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28711897"
---
# <a name="reshaping"></a><span data-ttu-id="0d2f9-102">Remodelagem</span><span class="sxs-lookup"><span data-stu-id="0d2f9-102">Reshaping</span></span>

<span data-ttu-id="0d2f9-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="0d2f9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0d2f9-p101">A um **Recordset** criado por uma cláusula de um comando shape pode ser atribuído um nome de *alias* (geralmente com a palavra-chave AS). O alias de um **Recordset** com forma pode ser mencionado em um comando totalmente diferente. Ou seja, você pode usar novamente ou *alterar a forma* de um **Recordset** com formato anterior em um novo comando shape. Para oferecer suporte a este recurso, o ADO fornece uma propriedade, [Reshape Name](reshape-name-property-dynamic-ado.md).</span><span class="sxs-lookup"><span data-stu-id="0d2f9-p101">A **Recordset** created by a clause of a shape command may be assigned an *alias* name (typically with the AS keyword). The alias of a shaped **Recordset** can be referenced in an entirely different command. That is, you may reuse, or *reshape*, a previously shaped **Recordset** in a new shape command. To support this feature, ADO provides a property, [Reshape Name](reshape-name-property-dynamic-ado.md).</span></span>

<span data-ttu-id="0d2f9-p102">A alteração da forma tem duas funções principais. A primeira é associar um **Recordset** existente a um novo **Recordset** pai.</span><span class="sxs-lookup"><span data-stu-id="0d2f9-p102">Reshaping has two main functions. The first is to associate an existing **Recordset** with a new parent **Recordset**.</span></span>

## <a name="example"></a><span data-ttu-id="0d2f9-110">Exemplo</span><span class="sxs-lookup"><span data-stu-id="0d2f9-110">Example</span></span>

```vb 
 
. . . 
rs1.Open "SHAPE {select * from Customers} " & _ 
 "APPEND ({select * from Orders} AS chapOrders " & _ 
 "RELATE CustomerID to CustomerID)", cn 
 
rs2.Open "SHAPE {select * from Employees} " & _ 
 "APPEND (chapOrders RELATE EmployeeID to EmployeeID)", cn 
. . . 
```

<span data-ttu-id="0d2f9-111">A segunda função é para permitir o acesso não dividido em objetos de **Recordset** filho existentes, usando a sintaxe `"SHAPE <recordset reshape name>"`.</span><span class="sxs-lookup"><span data-stu-id="0d2f9-111">The second function is to enable non-chaptered access to existing child **Recordset** objects, using the syntax `"SHAPE <recordset reshape name>"`.</span></span>

> [!NOTE]
> <span data-ttu-id="0d2f9-112">[!OBSERVAçãO] Você não pode anexar colunas a um **Recordset** existente, alterar a forma de um **Recordset** parametrizado nem os objetos **Recordset** em qualquer cláusula COMPUTE intermediária ou executar operações agregadas em qualquer **Recordset** descendente a partir do **Recordset** que está tendo sua forma alterada.</span><span class="sxs-lookup"><span data-stu-id="0d2f9-112">You cannot append columns to an existing **Recordset**, reshape a parameterized **Recordset** or the **Recordset** objects in any intervening COMPUTE clause, or perform aggregate operations on any **Recordset** descendant from the **Recordset** being reshaped.</span></span> <span data-ttu-id="0d2f9-113">O **Recordset** sendo reformatado e a nova forma command ambos devem usar os mesmos \* \* o objeto de[Conexão](connection-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="0d2f9-113">The **Recordset** being reshaped and the new shape command must both use the same \*\*[Connection](connection-object-ado.md) object.</span></span>


