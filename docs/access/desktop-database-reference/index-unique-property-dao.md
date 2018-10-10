---
title: Propriedade Index.Unique (DAO)
TOCTitle: Unique Property
ms:assetid: a4486da5-8a1a-b4fc-0e07-e65cd2e726f6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821087(v=office.15)
ms:contentKeyID: 48546809
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052990
f1_categories:
- Office.Version=v15
ms.openlocfilehash: bf2bbd8e1bf5c7c51d93e0669becbfd093e29994
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464664"
---
# <a name="indexunique-property-dao"></a><span data-ttu-id="6c0fa-102">Propriedade Index.Unique (DAO)</span><span class="sxs-lookup"><span data-stu-id="6c0fa-102">Index.Unique Property (DAO)</span></span>

<span data-ttu-id="6c0fa-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="6c0fa-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="6c0fa-104">Define ou retorna um valor que indica se objeto **[Index](index-object-dao.md)** representa um índice (chave) exclusivo para uma tabela (somente em espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="6c0fa-104">Sets or returns a value that indicates whether an **[Index](index-object-dao.md)** object represents a unique (key) index for a table (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="6c0fa-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6c0fa-105">Syntax</span></span>

<span data-ttu-id="6c0fa-106">*expressão* . Exclusivo</span><span class="sxs-lookup"><span data-stu-id="6c0fa-106">*expression* .Unique</span></span>

<span data-ttu-id="6c0fa-107">*expressão* Uma variável que representa um objeto **Index** .</span><span class="sxs-lookup"><span data-stu-id="6c0fa-107">*expression* A variable that represents an **Index** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c0fa-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="6c0fa-108">Remarks</span></span>

<span data-ttu-id="6c0fa-109">Essa definição de propriedade será leitura/gravação até que objeto seja acrescentado a uma coleção; depois disso, será somente leitura.</span><span class="sxs-lookup"><span data-stu-id="6c0fa-109">This property setting is read/write until the object is appended to a collection, after which it's read-only.</span></span>

<span data-ttu-id="6c0fa-p101">Um índice exclusivo é composto de um ou vários campos que organizam, de forma lógica, todos os registros em uma tabela em uma ordem exclusiva e predefinida. Se o índice for composto de um campo, os valores desse campo deverão ser exclusivos para a tabela inteira. Se o índice for composto por mais de um campo, cada campo conterá os valores duplicados, mas cada combinação de valores de todos os campos indexados deverá ser exclusiva.</span><span class="sxs-lookup"><span data-stu-id="6c0fa-p101">A unique index consists of one or more fields that logically arrange all records in a table in a unique, predefined order. If the index consists of one field, values in that field must be unique for the entire table. If the index consists of more than one field, each field can contain duplicate values, but each combination of values from all the indexed fields must be unique.</span></span>

<span data-ttu-id="6c0fa-p102">Se ambas as propriedades **Unique** e **[Primary](index-primary-property-dao.md)** de um objeto **Index** estiverem definidas como **True**, o índice será exclusivo e primário: identificará exclusivamente todos os registros da tabela em uma ordem lógica e predefinida. Se a propriedade **Primary** estiver definida como **False**, o índice será um índice secundário. Os índices secundários (ambos chave e não chave) organizam logicamente os registros em uma ordem predefinida sem servirem de identificadores para os registros de uma tabela.</span><span class="sxs-lookup"><span data-stu-id="6c0fa-p102">If both the **Unique** and **[Primary](index-primary-property-dao.md)** properties of an **Index** object are set to **True**, the index is unique and primary: It uniquely identifies all records in the table in a predefined, logical order. If the **Primary** property is set to **False**, the index is a secondary index. Secondary indexes (both key and nonkey) logically arrange records in a predefined order without serving as an identifier for records in the table.</span></span>


> [!NOTE]
> <UL>
> <LI>
> <P><span data-ttu-id="6c0fa-116">Não é necessário criar índices para tabelas mas, em tabelas grandes e não indexadas, o acesso a um registro específico pode demorar muito tempo.</span><span class="sxs-lookup"><span data-stu-id="6c0fa-116">You don't have to create indexes for tables, but in large, unindexed tables, accessing a specific record can take a long time.</span></span></P>
> <LI>
> <P><span data-ttu-id="6c0fa-117">Os registros recuperados das tabelas sem os índices não são retornados em uma sequência específica.</span><span class="sxs-lookup"><span data-stu-id="6c0fa-117">Records retrieved from tables without indexes are returned in no particular sequence.</span></span></P>
> <LI>
> <P><span data-ttu-id="6c0fa-118">A propriedade <STRONG><A href="field-attributes-property-dao.md">Attributes</A></STRONG> de cada objeto <STRONG><A href="field-object-dao.md">Field</A></STRONG> no objeto <STRONG>Index</STRONG> determina a ordem dos registros e, consequentemente, determina as técnicas de acesso para uso desse objeto <STRONG>Index</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="6c0fa-118">The <STRONG><A href="field-attributes-property-dao.md">Attributes</A></STRONG> property of each <STRONG><A href="field-object-dao.md">Field</A></STRONG> object in the <STRONG>Index</STRONG> object determines the order of records and consequently determines the access techniques to use for that <STRONG>Index</STRONG> object.</span></span></P>
> <LI>
> <P><span data-ttu-id="6c0fa-119">Um índice exclusivo ajuda a otimizar a localização de registros.</span><span class="sxs-lookup"><span data-stu-id="6c0fa-119">A unique index helps optimize finding records.</span></span></P>
> <LI>
> <P><span data-ttu-id="6c0fa-120">Os índices não afetem a ordem física de uma tabela base , afetam apenas a forma como os registros serão acessados pelo objeto <STRONG><A href="recordset-object-dao.md">Recordset</A></STRONG> do tipo tabela, quando um índice específico for escolhido ou quando o mecanismo de dados do Microsoft Access criar objetos <STRONG>Recordset</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="6c0fa-120">Indexes don't affect the physical order of a base table indexes affect only how the records are accessed by the table-type <STRONG><A href="recordset-object-dao.md">Recordset</A></STRONG> object when a particular index is chosen or when the Microsoft Access database engine creates <STRONG>Recordset</STRONG> objects.</span></span></P></LI></UL>



## <a name="example"></a><span data-ttu-id="6c0fa-121">Exemplo</span><span class="sxs-lookup"><span data-stu-id="6c0fa-121">Example</span></span>

<span data-ttu-id="6c0fa-p103">Este exemplo define a propriedade **Unique** de um novo objeto **Index** como **True** e acrescenta-o à coleção **Indexes** da tabela Funcionários. Em seguida, enumera a coleção **Indexes** da coleção **TableDef** e da coleção **Properties** de cada objeto **Index**. O novo objeto **Index** permitirá somente um registro com uma combinação específica de Country, LastName e FirstName no objeto **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="6c0fa-p103">This example sets the **Unique** property of a new **Index** object to **True**, and appends the Index to the **Indexes** collection of the Employees table. It then enumerates the **Indexes** collection of the **TableDef** and the **Properties** collection of each **Index**. The new **Index** will only allow one record with a particular combination of Country, LastName, and FirstName in the **TableDef**.</span></span>

```vb
    Sub UniqueX() 
     
       Dim dbsNorthwind As Database 
       Dim tdfEmployees As TableDef 
       Dim idxNew As Index 
       Dim idxLoop As Index 
       Dim prpLoop As Property 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       Set tdfEmployees = dbsNorthwind!Employees 
     
       With tdfEmployees 
          ' Create and append new Index object to the Indexes  
          ' collection of the Employees table. 
          Set idxNew = .CreateIndex("NewIndex") 
     
          With idxNew 
             .Fields.Append .CreateField("Country") 
             .Fields.Append .CreateField("LastName") 
             .Fields.Append .CreateField("FirstName") 
             .Unique = True 
          End With 
     
          .Indexes.Append idxNew 
          .Indexes.Refresh 
     
          Debug.Print .Indexes.Count & " Indexes in " & _ 
             .Name & " TableDef" 
     
          ' Enumerate Indexes collection of Employees table. 
          For Each idxLoop In .Indexes 
             Debug.Print "  " & idxLoop.Name 
     
             ' Enumerate Properties collection of each Index  
             ' object. 
             For Each prpLoop In idxLoop.Properties 
                Debug.Print "    " & prpLoop.Name & _ 
                   " = " & IIf(prpLoop = "", "[empty]", prpLoop) 
             Next prpLoop 
     
          Next idxLoop 
     
          ' Delete new Index because this is a demonstration. 
          .Indexes.Delete idxNew.Name 
       End With 
     
       dbsNorthwind.Close 
     
    End Sub
```
