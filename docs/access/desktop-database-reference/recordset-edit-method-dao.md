---
title: Método Recordset.Edit (DAO)
TOCTitle: Edit Method
ms:assetid: a64d601b-f446-da40-0020-b99110a72872
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821175(v=office.15)
ms:contentKeyID: 48546850
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 82dc6e175c7168d5c1b042e85dce7b77aa96b575
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300536"
---
# <a name="recordsetedit-method-dao"></a><span data-ttu-id="263d4-102">Método Recordset.Edit (DAO)</span><span class="sxs-lookup"><span data-stu-id="263d4-102">Recordset.Edit method (DAO)</span></span>

<span data-ttu-id="263d4-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="263d4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="263d4-104">Copia o registro atual de um objeto **[Recordset](recordset-object-dao.md)** atualizável para o buffer de cópia para edição subsequente.</span><span class="sxs-lookup"><span data-stu-id="263d4-104">Copies the current record from an updatable **[Recordset](recordset-object-dao.md)** object to the copy buffer for subsequent editing.</span></span>

## <a name="syntax"></a><span data-ttu-id="263d4-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="263d4-105">Syntax</span></span>

<span data-ttu-id="263d4-106">*expressão* .Edit</span><span class="sxs-lookup"><span data-stu-id="263d4-106">expression  . Edit</span></span>

<span data-ttu-id="263d4-107">*expressão* Uma variável que representa um objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="263d4-107">*expression*  A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="263d4-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="263d4-108">Remarks</span></span>

<span data-ttu-id="263d4-p101">Depois de usar o método **Edit**, as alterações feitas nos campos do registro atual são copiadas para o buffer de cópia. Após fazer as alterações desejadas no registro, use o método **[Update](recordset-update-method-dao.md)** para salvar as alterações.</span><span class="sxs-lookup"><span data-stu-id="263d4-p101">Once you use the **Edit** method, changes made to the current record's fields are copied to the copy buffer. After you make the desired changes to the record, use the **[Update](recordset-update-method-dao.md)** method to save your changes.</span></span>

<span data-ttu-id="263d4-111">O registro atual permanece atual após o uso de **Edit**.</span><span class="sxs-lookup"><span data-stu-id="263d4-111">The current record remains current after you use **Edit**.</span></span>

> [!NOTE]
> <span data-ttu-id="263d4-112">Se você editar um registro e, em seguida, executar qualquer operação que mova para outro registro, mas sem utilizar primeiro **Update**, suas alterações serão perdidas sem aviso.</span><span class="sxs-lookup"><span data-stu-id="263d4-112">If you edit a record and then perform any operation that moves to another record, but without first using **Update**, your changes are lost without warning.</span></span> <span data-ttu-id="263d4-113">Além disso, se você fechar recordset ou encerrar o procedimento que declara o **Recordset** ou o objeto pai **[Database](database-object-dao.md)** ou **[Connection](connection-object-dao.md)**, seu registro editado será descartado sem aviso.</span><span class="sxs-lookup"><span data-stu-id="263d4-113">In addition, if you close  recordset or end the procedure which declares the **Recordset** or the parent [**Database**](connection-object-dao.md) or **Connection** object, your edited record is discarded without warning.</span></span>

<span data-ttu-id="263d4-114">Utilizar **Edit** produzirá um erro se:</span><span class="sxs-lookup"><span data-stu-id="263d4-114">Using **Edit** produces an error if:</span></span>

- <span data-ttu-id="263d4-115">Não houver nenhum registro.</span><span class="sxs-lookup"><span data-stu-id="263d4-115">There is no current record.</span></span>

- <span data-ttu-id="263d4-116">O objeto **Connection**, **Database** ou **Recordset** tiver sido aberto como somente leitura.</span><span class="sxs-lookup"><span data-stu-id="263d4-116">The **Connection**, **Database**, or **Recordset** object was opened as read-only.</span></span>

- <span data-ttu-id="263d4-117">Nenhum campo no registro for atualizável.</span><span class="sxs-lookup"><span data-stu-id="263d4-117">No fields in the record are updatable.</span></span>

- <span data-ttu-id="263d4-118">O **Database** ou o **Recordset** tiver sido aberto para ser utilizado exclusivamente por outro usuário (espaço de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="263d4-118">The **Database** or **Recordset** was opened for exclusive use by another user (Microsoft Access workspace).</span></span>

- <span data-ttu-id="263d4-119">Outro usuário bloqueou a página contendo seu registro (espaço de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="263d4-119">Another user has locked the page containing your record (Microsoft Access workspace).</span></span>

<span data-ttu-id="263d4-p103">Em um espaço de trabalho do Microsoft Access, quando a configuração da propriedade [**LockEdits**](recordset-lockedits-property-dao.md) do objeto **Recordset** é **True** (bloqueado de forma pessimista) em um ambiente de vários usuários, o registro permanece bloqueado desde o momento em que **Edit** é usado até que a atualização seja concluída. Se a configuração da propriedade **LockEdits** for **False** (bloqueado de forma otimista), o registro será bloqueado e comparado ao registro pré-editado antes de ele ser atualizado no banco de dados. Se o registro foi alterado desde que você usou o método **Edit**, a operação **Update** falha com um erro de tempo de execução, se você usar **OpenRecordset** sem especificar **dbSeeChanges**. Por padrão, os bancos de dados ODBC e ISAM instalável conectados ao mecanismo de banco de dados do Microsoft Access sempre usam bloqueio otimista.</span><span class="sxs-lookup"><span data-stu-id="263d4-p103">In a Microsoft Access workspace, when the **Recordset** object's **[LockEdits](recordset-lockedits-property-dao.md)** property setting is **True** (pessimistically locked) in a multiuser environment, the record remains locked from the time **Edit** is used until the update is complete. If the **LockEdits** property setting is **False** (optimistically locked), the record is locked and compared with the pre-edited record just before it's updated in the database. If the record has changed since you used the **Edit** method, the **Update** operation fails with a run-time error if you use **OpenRecordset** without specifying **dbSeeChanges**. By default, Microsoft Access database engine-connected ODBC and installable ISAM databases always use optimistic locking.</span></span>

> [!NOTE]
> <span data-ttu-id="263d4-p104">Para adicionar, editar ou excluir um registro, deve haver um índice exclusivo no registro, na fonte de dados de base. Se não houver, um erro "Permissão negada" ocorrerá na chamada do método **[AddNew](recordset-addnew-method-dao.md)**, **[Delete](fields-delete-method-dao.md)** ou **Edit** em um espaço de trabalho do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="263d4-p104">To add, edit, or delete a record, there must be a unique index on the record in the underlying data source. If not, a "Permission denied" error will occur on the **[AddNew](recordset-addnew-method-dao.md)**, **[Delete](fields-delete-method-dao.md)**, or **Edit** method call in a Microsoft Access workspace.</span></span>

## <a name="example"></a><span data-ttu-id="263d4-126">Exemplo</span><span class="sxs-lookup"><span data-stu-id="263d4-126">Example</span></span>

<span data-ttu-id="263d4-p105">Este exemplo usa o método **Edit** para substituir os dados atuais pelo nome especificado. O procedimento EditName é exigido para que este procedimento seja executado.</span><span class="sxs-lookup"><span data-stu-id="263d4-p105">This example uses the **Edit** method to replace the current data with the specified name. The EditName procedure is required for this procedure to run.</span></span>

```vb
    Sub EditX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset 
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
     
    Sub EditName(rstTemp As Recordset, _ 
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
