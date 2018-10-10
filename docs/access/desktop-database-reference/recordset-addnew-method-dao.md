---
title: Método Recordset.AddNew (DAO)
TOCTitle: AddNew Method
ms:assetid: 18cb35f6-8652-fb20-2460-3d13fae39d23
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845624(v=office.15)
ms:contentKeyID: 48543483
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052883
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 8aee4e63959beca98e96d04d14f817b2b6a30e7c
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464065"
---
# <a name="recordsetaddnew-method-dao"></a><span data-ttu-id="f7fe7-102">Método Recordset.AddNew (DAO)</span><span class="sxs-lookup"><span data-stu-id="f7fe7-102">Recordset.AddNew Method (DAO)</span></span>


<span data-ttu-id="f7fe7-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="f7fe7-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="f7fe7-104">Cria um novo registro para um objeto **[Recordset](recordset-object-dao.md)** atualizável.</span><span class="sxs-lookup"><span data-stu-id="f7fe7-104">Creates a new record for an updatable **[Recordset](recordset-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7fe7-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f7fe7-105">Syntax</span></span>

<span data-ttu-id="f7fe7-106">*expressão* . AddNew</span><span class="sxs-lookup"><span data-stu-id="f7fe7-106">*expression* .AddNew</span></span>

<span data-ttu-id="f7fe7-107">*expressão* Uma variável que representa um objeto **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="f7fe7-107">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="f7fe7-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="f7fe7-108">Remarks</span></span>

<span data-ttu-id="f7fe7-p101">Use o método **AddNew** para criar e adicionar um novo registro no objeto **Recordset** com o nome do conjunto de registros. Este método define os campos como os valores padrão e, se nenhum valor padrão for especificado, ele definirá os campos como Nulo (os valores padrão especificados para um **Recordset** do tipo tabela).</span><span class="sxs-lookup"><span data-stu-id="f7fe7-p101">Use the **AddNew** method to create and add a new record in the **Recordset** object named by recordset. This method sets the fields to default values, and if no default values are specified, it sets the fields to Null (the default values specified for a table-type **Recordset**).</span></span>

<span data-ttu-id="f7fe7-p102">Depois de modificar o novo registro, use o método **[Update](recordset-update-method-dao.md)** para salvar as alterações e adicionar o registro ao **Recordset**. Não haverá alterações no banco de dados até você usar o método **Update**.</span><span class="sxs-lookup"><span data-stu-id="f7fe7-p102">After you modify the new record, use the **[Update](recordset-update-method-dao.md)** method to save the changes and add the record to the **Recordset**. No changes occur in the database until you use the **Update** method.</span></span>


> [!NOTE]
> <P><span data-ttu-id="f7fe7-p103">[!OBSERVAçãO] Se você emitir um <STRONG>AddNew</STRONG> e então executar qualquer operação que mova para outro registro, mas sem usar <STRONG>Update</STRONG>, suas alterações serão perdidas sem aviso. Além disso, se você fechar o <STRONG>Recordset</STRONG> ou encerrar o procedimento que declara o <STRONG>Recordset</STRONG> ou seu objeto <STRONG><A href="database-object-dao.md">Database</A></STRONG>, o novo registro será descartado sem aviso.</span><span class="sxs-lookup"><span data-stu-id="f7fe7-p103">If you issue an <STRONG>AddNew</STRONG> and then perform any operation that moves to another record, but without using <STRONG>Update</STRONG>, your changes are lost without warning. In addition, if you close the <STRONG>Recordset</STRONG> or end the procedure that declares the <STRONG>Recordset</STRONG> or its <STRONG><A href="database-object-dao.md">Database</A></STRONG> object, the new record is discarded without warning.</span></span></P>




> [!NOTE]
> <P><span data-ttu-id="f7fe7-p104">[!OBSERVAçãO] Quando você usa <STRONG>AddNew</STRONG> em um espaço de trabalho do Microsoft Access e o mecanismo de banco de dados tem de criar uma nova página para conter o registro atual, o bloqueio de página será pessimista. Se o novo registro se ajustar a uma página existente, o bloqueio de página será otimista.</span><span class="sxs-lookup"><span data-stu-id="f7fe7-p104">When you use <STRONG>AddNew</STRONG> in a Microsoft Access workspace and the database engine has to create a new page to hold the current record, page locking is pessimistic. If the new record fits in an existing page, page locking is optimistic.</span></span></P>



<span data-ttu-id="f7fe7-p105">Se você não tiver se movido para o último registro do seu **Recordset**, os registros adicionados a tabelas base por outros processos poderão ser incluídos caso tenham sido posicionados além do registro atual. No entanto, se você adicionar um registro ao seu próprio **Recordset**, o registro ficará visível no **Recordset** e será incluído na tabela subjacente onde se tornará visível para todos os objetos novos do **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="f7fe7-p105">If you haven't moved to the last record of your **Recordset**, records added to base tables by other processes may be included if they are positioned beyond the current record. If you add a record to your own **Recordset**, however, the record is visible in the **Recordset** and included in the underlying table where it becomes visible to any new **Recordset** objects.</span></span>

<span data-ttu-id="f7fe7-119">A posição do novo registro depende do tipo de **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="f7fe7-119">The position of the new record depends on the type of **Recordset**:</span></span>

  - <span data-ttu-id="f7fe7-120">Em um objeto **Recordset** do tipo dynaset, os registros são inseridos no final do **Recordset**, independentemente de qualquer regra de classificação ou de ordenação em vigor quando o **Recordset** tiver sido aberto.</span><span class="sxs-lookup"><span data-stu-id="f7fe7-120">In a dynaset-type **Recordset** object, records are inserted at the end of the **Recordset**, regardless of any sorting or ordering rules that were in effect when the **Recordset** was opened.</span></span>

  - <span data-ttu-id="f7fe7-p106">Em um objeto **Recordset** do tipo tabela cuja propriedade **[Index](recordset-index-property-dao.md)** tenha sido definida, os registros serão retornados no local apropriado na ordem de classificação. Se você não tiver definido a propriedade **Index**, os novos registros serão retornados no final do **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="f7fe7-p106">In a table-type **Recordset** object whose **[Index](recordset-index-property-dao.md)** property has been set, records are returned in their proper place in the sort order. If you haven't set the **Index** property, new records are returned at the end of the **Recordset**.</span></span>

<span data-ttu-id="f7fe7-p107">O registro que era o atual quando você usou o **AddNew** permanece atual. Se você quiser tornar o novo registro atual, poderá definir a propriedade **[Bookmark](recordset-bookmark-property-dao.md)** como o indicador identificado pela configuração da propriedade **[LastModified](recordset-lastmodified-property-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="f7fe7-p107">The record that was current before you used **AddNew** remains current. If you want to make the new record current, you can set the **[Bookmark](recordset-bookmark-property-dao.md)** property to the bookmark identified by the **[LastModified](recordset-lastmodified-property-dao.md)** property setting.</span></span>


> [!NOTE]
> <P><span data-ttu-id="f7fe7-p108">[!OBSERVAçãO] Para adicionar, editar ou excluir um registro, deve haver um índice exclusivo no registro na fonte de dados subjacente. Caso contrário, ocorrerá um erro "Permissão negada" na chamada ao método <STRONG>AddNew</STRONG>, <STRONG>Delete</STRONG> ou <STRONG>Edit</STRONG> em um espaço de trabalho do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="f7fe7-p108">To add, edit, or delete a record, there must be a unique index on the record in the underlying data source. If not, a "Permission denied" error will occur on the <STRONG>AddNew</STRONG>, <STRONG>Delete</STRONG>, or <STRONG>Edit</STRONG> method call in a Microsoft Access workspace.</span></span></P>



## <a name="example"></a><span data-ttu-id="f7fe7-127">Exemplo</span><span class="sxs-lookup"><span data-stu-id="f7fe7-127">Example</span></span>

<span data-ttu-id="f7fe7-p109">Este exemplo usa o método **AddNew** para criar um novo registro com o nome especificado. A função AddName é necessária para executar esse procedimento.</span><span class="sxs-lookup"><span data-stu-id="f7fe7-p109">This example uses the **AddNew** method to create a new record with the specified name. The AddName function is required for this procedure to run.</span></span>

```vb
    Sub AddNewX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset 
     Dim strFirstName As String 
     Dim strLastName As String 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees", dbOpenDynaset) 
     
     ' Get data from the user. 
     strFirstName = Trim(InputBox( _ 
     "Enter first name:")) 
     strLastName = Trim(InputBox( _ 
     "Enter last name:")) 
     
     ' Proceed only if the user actually entered something 
     ' for both the first and last names. 
     If strFirstName <> "" and strLastName <> "" Then 
     
     ' Call the function that adds the record. 
     AddName rstEmployees, strFirstName, strLastName 
     
     ' Show the newly added data. 
     With rstEmployees 
     Debug.Print "New record: " & !FirstName & _ 
     " " & !LastName 
     ' Delete new record because this is a demonstration. 
     .Delete 
     End With 
     
     Else 
     Debug.Print _ 
     "You must input a string for first and last name!" 
     End If 
     
     rstEmployees.Close 
     dbsNorthwind.Close 
     
    End Sub 
     
    Function AddName(rstTemp As Recordset, _ 
     strFirst As String, strLast As String) 
     
     ' Adds a new record to a Recordset using the data passed 
     ' by the calling procedure. The new record is then made 
     ' the current record. 
     With rstTemp 
     .AddNew 
     !FirstName = strFirst 
     !LastName = strLast 
     .Update 
     .Bookmark = .LastModified 
     End With 
     
    End Function
```
