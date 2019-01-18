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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28708841"
---
# <a name="recordsetedit-method-dao"></a>Método Recordset.Edit (DAO)

**Aplica-se a**: Access 2013, o Office 2013

Copia o registro atual de um objeto **[Recordset](recordset-object-dao.md)** atualizável para o buffer de cópia para edição subsequente.

## <a name="syntax"></a>Sintaxe

*expressão* . Editar

*expressão* Uma variável que representa um objeto **Recordset** .

## <a name="remarks"></a>Comentários

Assim que você usar o método **Edit**, as alterações feitas nos campos do registro atual serão copiadas no buffer de cópia. Depois de fazer as alterações desejadas no registro, use o método **[Update](recordset-update-method-dao.md)** para salvar suas alterações.

O registro atual continua sendo atual depois do uso de **Edit**.

> [!NOTE]
> [!OBSERVAçãO] Se você editar um registro e, em seguida, realizar qualquer operação que mova para outro registro, mas sem usar antes **Update**, suas alterações serão perdidas sem aviso. Além disso, se você fechar o recordset ou encerrar o procedimento que declara o **Recordset** ou o objeto de **[banco de dados](database-object-dao.md)** ou **[Conexão](connection-object-dao.md)** pai, o seu registro editado é desconsiderado sem aviso.

O uso de **Edit** produzirá um erro se :

- Não houver registro atual.

- O objeto **Connection**, **Database** ou **Recordset** tiver sido aberto somente para leitura.

- Nenhum campo no registro for atualizável.

- O **Database** ou **Recordset** tiver sido aberto para uso exclusivo por outro usuário (espaço de trabalho do Microsoft Access).

- Outro usuário tiver protegido a página que contém seu registro (espaço de trabalho do Microsoft Access).

Em um espaço de trabalho do Microsoft Access, quando a configuração da propriedade [**LockEdits**](recordset-lockedits-property-dao.md) do objeto **Recordset** é **True** (bloqueado de forma pessimista) em um ambiente de vários usuários, o registro permanece bloqueado desde o momento em que **Edit** é usado até que a atualização seja concluída. Se a configuração da propriedade **LockEdits** for **False** (bloqueado de forma otimista), o registro será bloqueado e comparado ao registro pré-editado antes de ele ser atualizado no banco de dados. Se o registro foi alterado desde que você usou o método **Edit**, a operação **Update** falha com um erro de tempo de execução, se você usar **OpenRecordset** sem especificar **dbSeeChanges**. Por padrão, os bancos de dados ODBC e ISAM instalável conectados ao mecanismo de banco de dados do Microsoft Access sempre usam bloqueio otimista.

> [!NOTE]
> [!OBSERVAçãO] Para adicionar, editar ou excluir um registro, deve haver um índice único no registro na fonte de dados subjacente. Se não houver, ocorrerá um erro de "Permissão negada" na chamada do método **[AddNew](recordset-addnew-method-dao.md)**, **[Delete](fields-delete-method-dao.md)** ou **Edit** em um espaço de trabalho do Microsoft Access.

## <a name="example"></a>Exemplo

Este exemplo usa o método **Edit** para substituir o dado atual pelo nome especificado. O procedimento EditName é exigido para a execução deste procedimento.

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
