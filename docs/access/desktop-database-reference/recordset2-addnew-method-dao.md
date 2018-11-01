---
title: Método Recordset2.AddNew (DAO)
TOCTitle: AddNew Method
ms:assetid: 25c7d207-185c-943b-405e-b138ffb8b3e2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191874(v=office.15)
ms:contentKeyID: 48543792
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 274b32a53f6f2db53105b2ca5039efcf561c6d72
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870111"
---
# <a name="recordset2addnew-method-dao"></a><span data-ttu-id="e20b5-102">Método Recordset2.AddNew (DAO)</span><span class="sxs-lookup"><span data-stu-id="e20b5-102">Recordset2.AddNew Method (DAO)</span></span>


<span data-ttu-id="e20b5-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="e20b5-103">**Applies to**: Access 2013, Office 2013</span></span>
 

<span data-ttu-id="e20b5-104">Cria um novo registro para um objeto **Recordset2** atualizável.</span><span class="sxs-lookup"><span data-stu-id="e20b5-104">Creates a new record for an updatable **Recordset2** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="e20b5-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e20b5-105">Syntax</span></span>

<span data-ttu-id="e20b5-106">*expressão* . AddNew</span><span class="sxs-lookup"><span data-stu-id="e20b5-106">*expression* .AddNew</span></span>

<span data-ttu-id="e20b5-107">*expressão* Uma variável que representa um objeto **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="e20b5-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="e20b5-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="e20b5-108">Remarks</span></span>

<span data-ttu-id="e20b5-p101">Use o método **AddNew** para criar e adicionar um novo registro ao objeto **Recordset2** denominado por recordset. Este método define valores padrão para os campos e, se nenhum valor padrão estiver especificado, ele definirá os campos como nulos (os valores padrão especificados para um **Recordset2** do tipo tabela).</span><span class="sxs-lookup"><span data-stu-id="e20b5-p101">Use the **AddNew** method to create and add a new record in the **Recordset2** object named by recordset. This method sets the fields to default values, and if no default values are specified, it sets the fields to Null (the default values specified for a table-type **Recordset2**).</span></span>

<span data-ttu-id="e20b5-p102">Depois de modificar o novo registro, use o método **[Update](recordset2-update-method-dao.md)** para salvar as alterações e adicionar o registro ao **Recordset2**. Nenhuma alteração ocorrerá no banco de dados até você usar o método **Update**.</span><span class="sxs-lookup"><span data-stu-id="e20b5-p102">After you modify the new record, use the **[Update](recordset2-update-method-dao.md)** method to save the changes and add the record to the **Recordset2**. No changes occur in the database until you use the **Update** method.</span></span>


> [!NOTE]
> <P><span data-ttu-id="e20b5-p103">[!OBSERVAçãO] Se você emitir um <STRONG>AddNew</STRONG> e, em seguida, executar qualquer operação que mova para outro registro, mas sem usar <STRONG>Update</STRONG>, suas alterações serão perdidas sem aviso. Além disso, se você fechar o <STRONG>Recordset2</STRONG> ou concluir o procedimento que declara o <STRONG>Recordset2</STRONG> ou seu objeto <STRONG><A href="database-object-dao.md">Database</A></STRONG>, o novo registro será descartado sem aviso.</span><span class="sxs-lookup"><span data-stu-id="e20b5-p103">If you issue an <STRONG>AddNew</STRONG> and then perform any operation that moves to another record, but without using <STRONG>Update</STRONG>, your changes are lost without warning. In addition, if you close the <STRONG>Recordset2</STRONG> or end the procedure that declares the <STRONG>Recordset2</STRONG> or its <STRONG><A href="database-object-dao.md">Database</A></STRONG> object, the new record is discarded without warning.</span></span></P>




> [!NOTE]
> <P><span data-ttu-id="e20b5-p104">[!OBSERVAçãO] Quando você usa <STRONG>AddNew</STRONG> em um espaço de trabalho do Microsoft Access e o mecanismo de banco de dados tem que criar uma nova página para o registro atual, o bloqueio de página é pessimista. Se o novo registro couber em uma página existente, o bloqueio de página será otimista.</span><span class="sxs-lookup"><span data-stu-id="e20b5-p104">When you use <STRONG>AddNew</STRONG> in a Microsoft Access workspace and the database engine has to create a new page to hold the current record, page locking is pessimistic. If the new record fits in an existing page, page locking is optimistic.</span></span></P>



<span data-ttu-id="e20b5-p105">Se você não tiver movido para o último registro do seu **Recordset2**, os registros adicionados a tabelas base por outros processos poderão ser incluídos se estiverem posicionados além do registro atual. Se você adicionar um registro a seu próprio **Recordset2**, no entanto, o registro estará visível no **Recordset2** e incluído na tabela subjacente onde se tornará visível para quaisquer novos objetos **Recordset2**.</span><span class="sxs-lookup"><span data-stu-id="e20b5-p105">If you haven't moved to the last record of your **Recordset2**, records added to base tables by other processes may be included if they are positioned beyond the current record. If you add a record to your own **Recordset2**, however, the record is visible in the **Recordset2** and included in the underlying table where it becomes visible to any new **Recordset2** objects.</span></span>

<span data-ttu-id="e20b5-119">A posição do novo registro depende do tipo do **Recordset2**:</span><span class="sxs-lookup"><span data-stu-id="e20b5-119">The position of the new record depends on the type of **Recordset2**:</span></span>

  - <span data-ttu-id="e20b5-120">Em um objeto **Recordset2** do tipo dynaset, registros são inseridos no fim do **Recordset**, independentemente de qualquer regra de classificação ou ordenação aplicada quando o **Recordset** foi aberto.</span><span class="sxs-lookup"><span data-stu-id="e20b5-120">In a dynaset-type **Recordset2** object, records are inserted at the end of the **Recordset**, regardless of any sorting or ordering rules that were in effect when the **Recordset** was opened.</span></span>

  - <span data-ttu-id="e20b5-p106">Em um objeto **Recordset2** do tipo tabela cuja propriedade **[Index](recordset2-index-property-dao.md)** tiver sido definida, os registros serão retornados em seu próprio lugar na ordem de classificação. Se você não tiver definido a propriedade **Index**, novos registros serão retornados no fim do **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="e20b5-p106">In a table-type **Recordset2** object whose **[Index](recordset2-index-property-dao.md)** property has been set, records are returned in their proper place in the sort order. If you haven't set the **Index** property, new records are returned at the end of the **Recordset**.</span></span>

<span data-ttu-id="e20b5-p107">O registro que era o atual antes de você usar o **AddNew** continuará sendo o atual. Se desejar tornar o novo registro atual, você poderá definir a propriedade **[Bookmark](recordset2-bookmark-property-dao.md)** para o indicador identificado pela configuração da propriedade **[LastModified](recordset2-lastmodified-property-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="e20b5-p107">The record that was current before you used **AddNew** remains current. If you want to make the new record current, you can set the **[Bookmark](recordset2-bookmark-property-dao.md)** property to the bookmark identified by the **[LastModified](recordset2-lastmodified-property-dao.md)** property setting.</span></span>


> [!NOTE]
> <P><span data-ttu-id="e20b5-p108">[!OBSERVAçãO] Para adicionar, editar ou excluir um registro, deve haver um índice exclusivo no registro na fonte de dados subjacente. Caso contrário, ocorrerá um erro "Permissão negada" na chamada ao método <STRONG>AddNew</STRONG>, <STRONG>Delete</STRONG> ou <STRONG>Edit</STRONG> em um espaço de trabalho do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="e20b5-p108">To add, edit, or delete a record, there must be a unique index on the record in the underlying data source. If not, a "Permission denied" error will occur on the <STRONG>AddNew</STRONG>, <STRONG>Delete</STRONG>, or <STRONG>Edit</STRONG> method call in a Microsoft Access workspace.</span></span></P>



## <a name="example"></a><span data-ttu-id="e20b5-127">Exemplo</span><span class="sxs-lookup"><span data-stu-id="e20b5-127">Example</span></span>

<span data-ttu-id="e20b5-p109">Este exemplo usa o método **AddNew** para criar um novo registro com o nome especificado. A função AddName é necessária para executar esse procedimento.</span><span class="sxs-lookup"><span data-stu-id="e20b5-p109">This example uses the **AddNew** method to create a new record with the specified name. The AddName function is required for this procedure to run.</span></span>

```vb
    Sub AddNewX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset2 
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
     
    Function AddName(rstTemp As Recordset2, _ 
     strFirst As String, strLast As String) 
     
     ' Adds a new record to a recordset using the data passed 
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
