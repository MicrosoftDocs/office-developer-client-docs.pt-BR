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
ms.openlocfilehash: 3f55107988002cf5718eac5eb445529f5c4e3e98
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867773"
---
# <a name="recordset2edit-method-dao"></a>Método Recordset2.Edit (DAO)


**Aplica-se a**: Access 2013, o Office 2013

Copia o registro atual de um objeto **[Recordset](recordset-object-dao.md)** atualizável para o buffer de cópia para edição subsequente.

## <a name="syntax"></a>Sintaxe

*expressão* . Editar

*expressão* Uma variável que representa um objeto **Recordset2** .

## <a name="remarks"></a>Comentários

Assim que você usar o método **Edit**, as alterações feitas nos campos do registro atual serão copiadas no buffer de cópia. Depois de fazer as alterações desejadas no registro, use o método **[Update](recordset2-update-method-dao.md)** para salvar suas alterações.

O registro atual continua sendo atual depois do uso de **Edit**.


> [!NOTE]
> <P>[!OBSERVAçãO] Se você editar um registro e, em seguida, realizar qualquer operação que mova para outro registro, mas sem usar antes <STRONG>Update</STRONG>, suas alterações serão perdidas sem aviso. Além disso, se você fechar o recordset ou encerrar o procedimento que declara o <STRONG>Recordset</STRONG> ou o objeto de <STRONG><A href="database-object-dao.md">banco de dados</A></STRONG> ou <STRONG><A href="connection-object-dao.md">Conexão</A></STRONG> pai, o seu registro editado é desconsiderado sem aviso.</P>



O uso de **Edit** produzirá um erro se :

  - Não houver registro atual.

  - O objeto **Connection**, **Database** ou **Recordset** tiver sido aberto somente para leitura.

  - Nenhum campo no registro for atualizável.

  - O **Database** ou **Recordset** tiver sido aberto para uso exclusivo por outro usuário (espaço de trabalho do Microsoft Access).

  - Outro usuário tiver protegido a página que contém seu registro (espaço de trabalho do Microsoft Access).

Em um espaço de trabalho do Microsoft Access, quando a configuração da propriedade [**LockEdits**](recordset2-lockedits-property-dao.md) do objeto **Recordset** é **True** (bloqueado de forma pessimista) em um ambiente de vários usuários, o registro permanece bloqueado desde o momento em que **Edit** é usado até que a atualização seja concluída. Se a configuração da propriedade **LockEdits** for **False** (bloqueado de forma otimista), o registro será bloqueado e comparado ao registro pré-editado antes de ele ser atualizado no banco de dados. Se o registro foi alterado desde que você usou o método **Edit**, a operação **Update** falha com um erro de tempo de execução, se você usar **OpenRecordset** sem especificar **dbSeeChanges**. Por padrão, os bancos de dados ODBC e ISAM instalável conectados ao mecanismo de banco de dados do Microsoft Access sempre usam bloqueio otimista.


> [!NOTE]
> <P>[!OBSERVAçãO] Para adicionar, editar ou excluir um registro, deve haver um índice único no registro na fonte de dados subjacente. Se não houver, ocorrerá um erro de "Permissão negada" na chamada do método <STRONG><A href="recordset2-addnew-method-dao.md">AddNew</A></STRONG>, <STRONG><A href="fields-delete-method-dao.md">Delete</A></STRONG> ou <STRONG>Edit</STRONG> em um espaço de trabalho do Microsoft Access.</P>



## <a name="example"></a>Exemplo

Este exemplo usa o método **Edit** para substituir o dado atual pelo nome especificado. O procedimento EditName é exigido para a execução deste procedimento.

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
