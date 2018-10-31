---
title: Data Shaping (referência de banco de dados da área de trabalho do Access)
TOCTitle: Data Shaping
ms:assetid: 650571cc-6874-2cdb-dd76-0804d1cc4e38
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249390(v=office.15)
ms:contentKeyID: 48545305
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 686c860ef9d8975b02391fedcea8f4b6f4e0b9bb
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25862293"
---
# <a name="data-shaping"></a><span data-ttu-id="c9b00-102">Data Shaping</span><span class="sxs-lookup"><span data-stu-id="c9b00-102">Data Shaping</span></span>


<span data-ttu-id="c9b00-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="c9b00-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="c9b00-104">A forma dos dados permite definir as colunas de um **Recordset** formado, as relações entre as entidades representadas pelas colunas e a maneira na qual o **Recordset** é preenchido com dados.</span><span class="sxs-lookup"><span data-stu-id="c9b00-104">Data shaping enables you to define the columns of a shaped **Recordset**, the relationships between the entities represented by the columns, and the manner in which the **Recordset** is populated with data.</span></span>

<span data-ttu-id="c9b00-105">As colunas de um **Recordset** formado podem conter dados de um provedor de dados como o Microsoft SQL Server, referência a outro **Recordset**, valores derivados de um cálculo em uma única linha de um **Recordset**, valores derivados de uma operação sobre uma coluna de um **Recordset** inteiro; ou pode ser uma coluna vazia recém-fabricada.</span><span class="sxs-lookup"><span data-stu-id="c9b00-105">Columns of a shaped **Recordset** may contain data from a data provider such as Microsoft SQL Server, references to another **Recordset**, values derived from a calculation on a single row of a **Recordset**, values derived from an operation over a column of an entire **Recordset**; or they may be a newly fabricated, empty column.</span></span>

<span data-ttu-id="c9b00-p101">Ao recuperar o valor de uma coluna que contenha uma referência a outro **Recordset**, o ADO retorna automaticamente o **Recordset** real representado pela referência. Um **Recordset** que contém outro **Recordset** é chamado de conjunto de registro hierárquico. Os conjuntos de registro hierárquicos exibem uma relação *pai-filho*, no qual o *pai* é o conjunto de registro que contém e o *filho* é o conjunto de registro contido. A referência a um **Recordset** é, na realidade, uma referência a um subconjunto do filho, chamado de *capítulo*. Um único pai pode fazer referência a mais de um filho **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="c9b00-p101">When you retrieve the value of a column that contains a reference to another **Recordset**, ADO automatically returns the actual **Recordset** represented by the reference. A **Recordset** that contains another **Recordset** is called a hierarchical recordset. Hierarchical recordsets exhibit a *parent-child* relationship, in which the *parent* is the containing recordset and the *child* is the contained recordset. The reference to a **Recordset** is actually a reference to a subset of the child, called a *chapter*. A single parent may reference more than one child **Recordset**.</span></span>

<span data-ttu-id="c9b00-p102">A sintaxe do comando shape permite criar programaticamente um **Recordset** formado. Em seguida, você pode acessar os componentes do **Recordset** programaticamente ou através de um controle visual apropriado. Um comando shape é emitido como qualquer outro texto de comando ADO.</span><span class="sxs-lookup"><span data-stu-id="c9b00-p102">The shape command syntax enables you to programmatically create a shaped **Recordset**. You can then access the components of the **Recordset** programmatically or through an appropriate visual control. A shape command is issued like any other ADO command text.</span></span>

<span data-ttu-id="c9b00-p103">Você pode tornar objetos **Recordset** hierárquicos de duas maneiras com a sintaxe do comando shape. A primeira anexa um **Recordset** filho a um **Recordset** pai. O pai e o filho geralmente possuem, no mínimo, uma coluna em comum: o valor da coluna em uma linha do pai tem o mesmo valor da coluna em todas as linhas do filho.</span><span class="sxs-lookup"><span data-stu-id="c9b00-p103">You can make hierarchical **Recordset** objects in two ways with the shape command syntax. The first appends a child **Recordset** to a parent **Recordset**. The parent and child typically have at least one column in common: the value of the column in a row of the parent is the same as the value of the column in all rows of the child.</span></span>

<span data-ttu-id="c9b00-p104">A segunda maneira gera um **Recordset** pai de um **Recordset** filho. Os registros no **Recordset** filho são agrupados, geralmente usando a cláusula BY e uma linha é adicionada ao **Recordset** pai para cada grupo resultante no filho. Se a cláusula BY for omitida, o **Recordset** filho formará um único grupo e o **Recordset** pai conterá exatamente uma linha. Isso é útil para calcular os agregados do "grand total" sobre o **Recordset** filho inteiro.</span><span class="sxs-lookup"><span data-stu-id="c9b00-p104">The second way generates a parent **Recordset** from a child **Recordset**. The records in the child **Recordset** are grouped, typically using the BY clause, and one row is added to the parent **Recordset** for each resulting group in the child. If the BY clause is omitted, the child **Recordset** will form a single group and the parent **Recordset** will contain exactly one row. This is useful for computing "grand total" aggregates over the entire child **Recordset**.</span></span>

<span data-ttu-id="c9b00-p105">Independentemente do **Recordset** pai que é formado, isso conterá uma coluna de capítulo que é usado para relacioná-lo ao **Recordset** filho. Se você desejar, o **Recordset** também pode ter colunas que contenham agregados (SUM, MIN, MAX e assim por diante) sobre as linhas filho. Tanto o **Recordset** pai como o filho que contêm uma expressão na linha no **Recordset**, bem como colunas que sejam novas e inicialmente vazias.</span><span class="sxs-lookup"><span data-stu-id="c9b00-p105">Regardless of which way the parent **Recordset** is formed, it will contain a chapter column that is used to relate it to a child **Recordset**. If you wish, the parent **Recordset** may also have columns that contain aggregates (SUM, MIN, MAX, and so on) over the child rows. Both the parent and the child **Recordset** may have columns which contain an expression on the row in the **Recordset**, as well as columns which are new and initially empty.</span></span>

<span data-ttu-id="c9b00-124">Você pode aninhar objetos **Recordset** hierárquicos a qualquer profundidade (ou seja, criar objetos **Recordset** filho de objetos **Recordset** filho e assim por diante).</span><span class="sxs-lookup"><span data-stu-id="c9b00-124">You can nest hierarchical **Recordset** objects to any depth (that is, create child **Recordset** objects of child **Recordset** objects, and so on).</span></span>

<span data-ttu-id="c9b00-125">Você pode acessar os componentes **Recordset** do **Recordset** formado de forma programática ou através de um controle visual apropriado.</span><span class="sxs-lookup"><span data-stu-id="c9b00-125">You can access the **Recordset** components of the shaped **Recordset** programmatically or through an appropriate visual control.</span></span>

<span data-ttu-id="c9b00-126">Para obter exemplos de comandos shape e suas hierarquias resultantes, consulte Usando o serviço de forma de dados para OLE DB: Uma visão geral melhor.</span><span class="sxs-lookup"><span data-stu-id="c9b00-126">For examples of shape commands and their resulting hierarchies, see Using the Data Shaping Service for OLE DB: A Closer Look.</span></span>

<span data-ttu-id="c9b00-127">Esta seção inclui os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="c9b00-127">This section includes the following topics:</span></span>

- [<span data-ttu-id="c9b00-128">Reformatação</span><span class="sxs-lookup"><span data-stu-id="c9b00-128">Reshaping</span></span>](reshaping.md)

- [<span data-ttu-id="c9b00-129">Agregados neto</span><span class="sxs-lookup"><span data-stu-id="c9b00-129">Grandchild Aggregates</span></span>](grandchild-aggregates.md)

- [<span data-ttu-id="c9b00-130">Comandos com parâmetros e comandos COMPUTE de intervenção</span><span class="sxs-lookup"><span data-stu-id="c9b00-130">Parameterized Commands with Intervening COMPUTE Commands</span></span>](parameterized-commands-with-intervening-compute-commands.md)

- [<span data-ttu-id="c9b00-131">Mantendo conjuntos de registros hierárquicos</span><span class="sxs-lookup"><span data-stu-id="c9b00-131">Persisting Hierarchical Recordsets</span></span>](persisting-hierarchical-recordsets.md)