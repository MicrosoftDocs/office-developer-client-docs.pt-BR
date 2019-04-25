---
title: Conjunto TableDefs (DAO)
TOCTitle: TableDefs Collection
ms:assetid: a2986b02-0437-d6ac-7bbb-c43f5225c3fc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff820997(v=office.15)
ms:contentKeyID: 48546766
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: f16f44b57a690aa58efdff9b00341df5023c293f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314172"
---
# <a name="tabledefs-collection-dao"></a><span data-ttu-id="2c014-102">Conjunto TableDefs (DAO)</span><span class="sxs-lookup"><span data-stu-id="2c014-102">TableDefs collection (DAO)</span></span>

<span data-ttu-id="2c014-103">**Se aplica a:** Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="2c014-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2c014-104">Um conjunto **TableDefs** contém todos os objetos **TableDef** armazenados em banco de dados (espaços de trabalho do Microsoft Access somente).</span><span class="sxs-lookup"><span data-stu-id="2c014-104">A **TableDefs** collection contains all stored **TableDef** objects in a database (Microsoft Access workspaces only).</span></span>

## <a name="remarks"></a><span data-ttu-id="2c014-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="2c014-105">Remarks</span></span>

<span data-ttu-id="2c014-106">Manipula-se a definição de uma tabela usando um objeto **TableDef** e seus métodos e propriedades.</span><span class="sxs-lookup"><span data-stu-id="2c014-106">You manipulate a table definition using a **TableDef** object and its methods and properties.</span></span>

<span data-ttu-id="2c014-107">A coleção padrão de um objeto **Database** é a coleção **TableDefs**.</span><span class="sxs-lookup"><span data-stu-id="2c014-107">The default collection of a **Database** object is the **TableDefs** collection.</span></span>

<span data-ttu-id="2c014-108">Para referir-se a um objeto **TableDef** de uma coleção pelo número ordinal ou pela configuração da propriedade **Name**, use qualquer uma das formas de sintaxe a seguir:</span><span class="sxs-lookup"><span data-stu-id="2c014-108">To refer to a **TableDef** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

<span data-ttu-id="2c014-109">**TableDefs**(0)</span><span class="sxs-lookup"><span data-stu-id="2c014-109">**TableDefs**(0)</span></span>

<span data-ttu-id="2c014-110">**TableDefs**("nome")</span><span class="sxs-lookup"><span data-stu-id="2c014-110">**TableDefs**("name")</span></span>

<span data-ttu-id="2c014-111">**TableDefs**\!\[nome\]</span><span class="sxs-lookup"><span data-stu-id="2c014-111">**TableDefs**\!\[name\]</span></span>

<span data-ttu-id="2c014-112">**Links fornecidos pela** comunidade [UtterAccess](https://www.utteraccess.com).</span><span class="sxs-lookup"><span data-stu-id="2c014-112">**Links provided by** the [UtterAccess](https://www.utteraccess.com) community.</span></span> <span data-ttu-id="2c014-113">UtterAccess é o fórum principal de wiki e de ajuda do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="2c014-113">UtterAccess is the premier Microsoft Access wiki and help forum.</span></span>

  - [<span data-ttu-id="2c014-114">Re-Vincular Back-ends Múltiplos</span><span class="sxs-lookup"><span data-stu-id="2c014-114">Re-Linker Multi-Backends</span></span>](https://www.utteraccess.com/wiki/index.php/re-linker_multi-backends)

  - [<span data-ttu-id="2c014-115">Trocar/Re-vincular Entre AO VIVO, TESTE e Dados LOCAIS</span><span class="sxs-lookup"><span data-stu-id="2c014-115">Swap/Relink Between LIVE, TEST and LOCAL Data</span></span>](https://www.utteraccess.com/forum/swap-relink-live-test-t1328573.html)

## <a name="example"></a><span data-ttu-id="2c014-116">Exemplo</span><span class="sxs-lookup"><span data-stu-id="2c014-116">Example</span></span>

<span data-ttu-id="2c014-p102">Este exemplo cria um novo objeto **TableDef** e o acrescenta à coleção **TableDefs** do objeto Database Northwind. Em seguida, enumeram-se as coleções **TableDefs** e **Properties** do novo **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="2c014-p102">This example creates a new **TableDef** object and appends it to the **TableDefs** collection of the Northwind Database object. It then enumerates the **TableDefs** collection and the **Properties** collection of the new **TableDef**.</span></span>

```vb
    Sub TableDefX() 
     
       Dim dbsNorthwind As Database 
       Dim tdfNew As TableDef 
       Dim tdfLoop As TableDef 
       Dim prpLoop As Property 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
       ' Create new TableDef object, append Field objects  
       ' to its Fields collection, and append TableDef  
       ' object to the TableDefs collection of the  
       ' Database object. 
       Set tdfNew = dbsNorthwind.CreateTableDef("NewTableDef") 
       tdfNew.Fields.Append tdfNew.CreateField("Date", dbDate) 
       dbsNorthwind.TableDefs.Append tdfNew 
     
       With dbsNorthwind 
          Debug.Print .TableDefs.Count & _ 
             " TableDefs in " & .Name 
     
          ' Enumerate TableDefs collection. 
          For Each tdfLoop In .TableDefs 
             Debug.Print "  " & tdfLoop.Name 
          Next tdfLoop 
     
          With tdfNew 
             Debug.Print "Properties of " & .Name 
     
             ' Enumerate Properties collection of new 
             ' TableDef object, only printing properties 
             ' with non-empty values. 
             For Each prpLoop In .Properties 
                Debug.Print "  " & prpLoop.Name & " - " & _ 
                   IIf(prpLoop = "", "[empty]", prpLoop) 
             Next prpLoop 
     
          End With 
     
          ' Delete new TableDef since this is a  
          ' demonstration. 
          .TableDefs.Delete tdfNew.Name 
          .Close 
       End With 
     
    End Sub 
```

<br/>

<span data-ttu-id="2c014-119">Este exemplo cria um novo objeto **TableDef** no banco de dados da Northwind.</span><span class="sxs-lookup"><span data-stu-id="2c014-119">This example creates a new **TableDef** object in the Northwind database.</span></span>

```vb 
Sub CreateTableDefX() 
 
   Dim dbsNorthwind As Database 
   Dim tdfNew As TableDef 
   Dim prpLoop As Property 
 
   Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 
   ' Create a new TableDef object. 
   Set tdfNew = dbsNorthwind.CreateTableDef("Contacts") 
 
   With tdfNew 
      ' Create fields and append them to the new TableDef  
      ' object. This must be done before appending the  
      ' TableDef object to the TableDefs collection of the  
      ' Northwind database. 
      .Fields.Append .CreateField("FirstName", dbText) 
      .Fields.Append .CreateField("LastName", dbText) 
      .Fields.Append .CreateField("Phone", dbText) 
      .Fields.Append .CreateField("Notes", dbMemo) 
 
      Debug.Print "Properties of new TableDef object " & _ 
         "before appending to collection:" 
 
      ' Enumerate Properties collection of new TableDef  
      ' object. 
      For Each prpLoop In .Properties 
         On Error Resume Next 
         If prpLoop <> "" Then Debug.Print "  " & _ 
           prpLoop.Name & " = " & prpLoop 
         On Error GoTo 0 
      Next prpLoop 
 
      ' Append the new TableDef object to the Northwind  
      ' database. 
      dbsNorthwind.TableDefs.Append tdfNew 
 
      Debug.Print "Properties of new TableDef object " & _ 
         "after appending to collection:" 
 
      ' Enumerate Properties collection of new TableDef  
      ' object. 
      For Each prpLoop In .Properties 
         On Error Resume Next 
         If prpLoop <> "" Then Debug.Print "  " & _ 
           prpLoop.Name & " = " & prpLoop 
         On Error GoTo 0 
      Next prpLoop 
 
   End With 
 
   ' Delete new TableDef object since this is a  
   ' demonstration. 
   dbsNorthwind.TableDefs.Delete "Contacts" 
 
   dbsNorthwind.Close 
 
```



