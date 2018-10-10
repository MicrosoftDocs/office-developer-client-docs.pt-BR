---
title: Método Recordset2.Edit (DAO)
TOCTitle: Edit Method
ms:assetid: 34c51eee-274d-3511-b5e2-cb74e4925ec8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192452(v=office.15)
ms:contentKeyID: 48544137
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052869
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 1255bd4aca0660cb6cb7baece5c569baa5bc1371
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25465117"
---
# <a name="recordset2edit-method-dao"></a><span data-ttu-id="f6751-102">Método Recordset2.Edit (DAO)</span><span class="sxs-lookup"><span data-stu-id="f6751-102">Recordset2.Edit Method (DAO)</span></span>


<span data-ttu-id="f6751-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="f6751-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="f6751-104">Copia o registro atual de um objeto **[Recordset](recordset-object-dao.md)** atualizável para o buffer de cópia para edição subsequente.</span><span class="sxs-lookup"><span data-stu-id="f6751-104">Copies the current record from an updatable **[Recordset](recordset-object-dao.md)** object to the copy buffer for subsequent editing.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6751-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f6751-105">Syntax</span></span>

<span data-ttu-id="f6751-106">*expressão* . Editar</span><span class="sxs-lookup"><span data-stu-id="f6751-106">*expression* .Edit</span></span>

<span data-ttu-id="f6751-107">*expressão* Uma variável que representa um objeto **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="f6751-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="f6751-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="f6751-108">Remarks</span></span>

<span data-ttu-id="f6751-p101">Assim que você usar o método **Edit**, as alterações feitas nos campos do registro atual serão copiadas no buffer de cópia. Depois de fazer as alterações desejadas no registro, use o método **[Update](recordset2-update-method-dao.md)** para salvar suas alterações.</span><span class="sxs-lookup"><span data-stu-id="f6751-p101">Once you use the **Edit** method, changes made to the current record's fields are copied to the copy buffer. After you make the desired changes to the record, use the **[Update](recordset2-update-method-dao.md)** method to save your changes.</span></span>

<span data-ttu-id="f6751-111">O registro atual continua sendo atual depois do uso de **Edit**.</span><span class="sxs-lookup"><span data-stu-id="f6751-111">The current record remains current after you use **Edit**.</span></span>


> [!NOTE]
> <P><span data-ttu-id="f6751-112">[!OBSERVAçãO] Se você editar um registro e, em seguida, realizar qualquer operação que mova para outro registro, mas sem usar antes <STRONG>Update</STRONG>, suas alterações serão perdidas sem aviso.</span><span class="sxs-lookup"><span data-stu-id="f6751-112">If you edit a record and then perform any operation that moves to another record, but without first using <STRONG>Update</STRONG>, your changes are lost without warning.</span></span> <span data-ttu-id="f6751-113">Além disso, se você fechar o recordset ou encerrar o procedimento que declara o <STRONG>Recordset</STRONG> ou o objeto de <STRONG><A href="database-object-dao.md">banco de dados</A></STRONG> ou <STRONG><A href="connection-object-dao.md">Conexão</A></STRONG> pai, o seu registro editado é desconsiderado sem aviso.</span><span class="sxs-lookup"><span data-stu-id="f6751-113">In addition, if you close recordset or end the procedure which declares the <STRONG>Recordset</STRONG> or the parent <STRONG><A href="database-object-dao.md">Database</A></STRONG> or <STRONG><A href="connection-object-dao.md">Connection</A></STRONG> object, your edited record is discarded without warning.</span></span></P>



<span data-ttu-id="f6751-114">O uso de **Edit** produzirá um erro se :</span><span class="sxs-lookup"><span data-stu-id="f6751-114">Using **Edit** produces an error if:</span></span>

  - <span data-ttu-id="f6751-115">Não houver registro atual.</span><span class="sxs-lookup"><span data-stu-id="f6751-115">There is no current record.</span></span>

  - <span data-ttu-id="f6751-116">O objeto **Connection**, **Database** ou **Recordset** tiver sido aberto somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="f6751-116">The **Connection**, **Database**, or **Recordset** object was opened as read-only.</span></span>

  - <span data-ttu-id="f6751-117">Nenhum campo no registro for atualizável.</span><span class="sxs-lookup"><span data-stu-id="f6751-117">No fields in the record are updatable.</span></span>

  - <span data-ttu-id="f6751-118">O **Database** ou **Recordset** tiver sido aberto para uso exclusivo por outro usuário (espaço de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="f6751-118">The **Database** or **Recordset** was opened for exclusive use by another user (Microsoft Access workspace).</span></span>

  - <span data-ttu-id="f6751-119">Outro usuário tiver protegido a página que contém seu registro (espaço de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="f6751-119">Another user has locked the page containing your record (Microsoft Access workspace).</span></span>

<span data-ttu-id="f6751-p103">Em um espaço de trabalho do Microsoft Access, quando a configuração da propriedade [**LockEdits**](recordset2-lockedits-property-dao.md) do objeto **Recordset** é **True** (bloqueado de forma pessimista) em um ambiente de vários usuários, o registro permanece bloqueado desde o momento em que **Edit** é usado até que a atualização seja concluída. Se a configuração da propriedade **LockEdits** for **False** (bloqueado de forma otimista), o registro será bloqueado e comparado ao registro pré-editado antes de ele ser atualizado no banco de dados. Se o registro foi alterado desde que você usou o método **Edit**, a operação **Update** falha com um erro de tempo de execução, se você usar **OpenRecordset** sem especificar **dbSeeChanges**. Por padrão, os bancos de dados ODBC e ISAM instalável conectados ao mecanismo de banco de dados do Microsoft Access sempre usam bloqueio otimista.</span><span class="sxs-lookup"><span data-stu-id="f6751-p103">In a Microsoft Access workspace, when the **Recordset** object's **[LockEdits](recordset2-lockedits-property-dao.md)** property setting is **True** (pessimistically locked) in a multiuser environment, the record remains locked from the time **Edit** is used until the update is complete. If the **LockEdits** property setting is **False** (optimistically locked), the record is locked and compared with the pre-edited record just before it's updated in the database. If the record has changed since you used the **Edit** method, the **Update** operation fails with a run-time error if you use **OpenRecordset** without specifying **dbSeeChanges**. By default, Microsoft Access database engine-connected ODBC and installable ISAM databases always use optimistic locking.</span></span>


> [!NOTE]
> <P><span data-ttu-id="f6751-p104">[!OBSERVAçãO] Para adicionar, editar ou excluir um registro, deve haver um índice único no registro na fonte de dados subjacente. Se não houver, ocorrerá um erro de "Permissão negada" na chamada do método <STRONG><A href="recordset2-addnew-method-dao.md">AddNew</A></STRONG>, <STRONG><A href="fields-delete-method-dao.md">Delete</A></STRONG> ou <STRONG>Edit</STRONG> em um espaço de trabalho do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="f6751-p104">To add, edit, or delete a record, there must be a unique index on the record in the underlying data source. If not, a "Permission denied" error will occur on the <STRONG><A href="recordset2-addnew-method-dao.md">AddNew</A></STRONG>, <STRONG><A href="fields-delete-method-dao.md">Delete</A></STRONG>, or <STRONG>Edit</STRONG> method call in a Microsoft Access workspace.</span></span></P>



## <a name="example"></a><span data-ttu-id="f6751-126">Exemplo</span><span class="sxs-lookup"><span data-stu-id="f6751-126">Example</span></span>

<span data-ttu-id="f6751-p105">Este exemplo usa o método **Edit** para substituir o dado atual pelo nome especificado. O procedimento EditName é exigido para a execução deste procedimento.</span><span class="sxs-lookup"><span data-stu-id="f6751-p105">This example uses the **Edit** method to replace the current data with the specified name. The EditName procedure is required for this procedure to run.</span></span>

```vb
    Sub EditX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset2 
     Dim strOldFirst As String 
     Dim strOldLast As String 
     Dim strFirstName As String 
     Dim strLastName As String 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees", _ 
     dbOpenDynaset) 
     
     ' Store original data. 
     strOldFirst = rstEmployees!FirstName 
     strOldLast = rstEmployees!LastName 
     
     ' Get new data for record. 
     strFirstName = Trim(InputBox( _ 
     "Enter first name:")) 
     strLastName = Trim(InputBox( _ 
     "Enter last name:")) 
     
     ' Proceed if the user entered something for both fields. 
     If strFirstName <> "" and strLastName <> "" Then 
     ' Update record with new data. 
     EditName rstEmployees, strFirstName, strLastName 
     
     With rstEmployees 
     ' Show old and new data. 
     Debug.Print "Old data: " & strOldFirst & _ 
     " " & strOldLast 
     Debug.Print "New data: " & !FirstName & _ 
     " " & !LastName 
     ' Restore original data because this is a 
     ' demonstration. 
     .Edit 
     !FirstName = strOldFirst 
     !LastName = strOldLast 
     .Update 
     End With 
     
     Else 
     Debug.Print _ 
     "You must input a string for first and last name!" 
     End If 
     
     rstEmployees.Close 
     dbsNorthwind.Close 
     
    End Sub 
     
    Sub EditName(rstTemp As Recordset2, _ 
     strFirst As String, strLast As String) 
     
     ' Make changes to record and set the bookmark to keep 
     ' the same record current. 
     With rstTemp 
     .Edit 
     !FirstName = strFirst 
     !LastName = strLast 
     .Update 
     .Bookmark = .LastModified 
     End With 
     
    End Sub
```
