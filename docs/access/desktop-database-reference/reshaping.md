---
title: Remodelagem (referência da área de trabalho do banco de dados do Access)
TOCTitle: Reshaping
ms:assetid: 89c6a0d6-3bf4-36ae-26ec-d4e60f920490
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249605(v=office.15)
ms:contentKeyID: 48546174
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a051c62d73a36fed0832f17b1cb53b1641d4a152
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25889277"
---
# <a name="reshaping"></a><span data-ttu-id="7f67e-102">Remodelagem</span><span class="sxs-lookup"><span data-stu-id="7f67e-102">Reshaping</span></span>


<span data-ttu-id="7f67e-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="7f67e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7f67e-p101">A um **Recordset** criado por uma cláusula de um comando shape pode ser atribuído um nome de *alias* (geralmente com a palavra-chave AS). O alias de um **Recordset** com forma pode ser mencionado em um comando totalmente diferente. Ou seja, você pode usar novamente ou *alterar a forma* de um **Recordset** com formato anterior em um novo comando shape. Para oferecer suporte a este recurso, o ADO fornece uma propriedade, [Reshape Name](reshape-name-property-dynamic-ado.md).</span><span class="sxs-lookup"><span data-stu-id="7f67e-p101">A **Recordset** created by a clause of a shape command may be assigned an *alias* name (typically with the AS keyword). The alias of a shaped **Recordset** can be referenced in an entirely different command. That is, you may reuse, or *reshape*, a previously shaped **Recordset** in a new shape command. To support this feature, ADO provides a property, [Reshape Name](reshape-name-property-dynamic-ado.md).</span></span>

<span data-ttu-id="7f67e-p102">A alteração da forma tem duas funções principais. A primeira é associar um **Recordset** existente a um novo **Recordset** pai.</span><span class="sxs-lookup"><span data-stu-id="7f67e-p102">Reshaping has two main functions. The first is to associate an existing **Recordset** with a new parent **Recordset**.</span></span>

## <a name="example"></a><span data-ttu-id="7f67e-110">Exemplo</span><span class="sxs-lookup"><span data-stu-id="7f67e-110">Example</span></span>

```vb 
 
. . . 
rs1.Open "SHAPE {select * from Customers} " & _ 
 "APPEND ({select * from Orders} AS chapOrders " & _ 
 "RELATE CustomerID to CustomerID)", cn 
 
rs2.Open "SHAPE {select * from Employees} " & _ 
 "APPEND (chapOrders RELATE EmployeeID to EmployeeID)", cn 
. . . 
```

<span data-ttu-id="7f67e-111">A segunda função é para permitir o acesso não dividido em objetos de **Recordset** filho existentes, usando a sintaxe `"SHAPE <recordset reshape name>"`.</span><span class="sxs-lookup"><span data-stu-id="7f67e-111">The second function is to enable non-chaptered access to existing child **Recordset** objects, using the syntax `"SHAPE <recordset reshape name>"`.</span></span>


> [!NOTE]
> <P><span data-ttu-id="7f67e-p103">[!OBSERVAçãO] Você não pode anexar colunas a um <STRONG>Recordset</STRONG> existente, alterar a forma de um <STRONG>Recordset</STRONG> parametrizado nem os objetos <STRONG>Recordset</STRONG> em qualquer cláusula COMPUTE intermediária ou executar operações agregadas em qualquer <STRONG>Recordset</STRONG> descendente a partir do <STRONG>Recordset</STRONG> que está tendo sua forma alterada. O <STRONG>Recordset</STRONG> que está tendo sua forma alterada e o novo comando shape devem usar a mesma <A href="connection-object-ado.md">Conexão</A>.</span><span class="sxs-lookup"><span data-stu-id="7f67e-p103">You cannot append columns to an existing <STRONG>Recordset</STRONG>, reshape a parameterized <STRONG>Recordset</STRONG> or the <STRONG>Recordset</STRONG> objects in any intervening COMPUTE clause, or perform aggregate operations on any <STRONG>Recordset</STRONG> descendant from the <STRONG>Recordset</STRONG> being reshaped. The <STRONG>Recordset</STRONG> being reshaped and the new shape command must both use the same <A href="connection-object-ado.md">Connection</A>.</span></span></P>


