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
# <a name="recordsetedit-method-dao"></a>Método Recordset.Edit (DAO)

**Aplica-se ao:** Access 2013, Office 2013

Copia o registro atual de um objeto **[Recordset](recordset-object-dao.md)** atualizável para o buffer de cópia para edição subsequente.

## <a name="syntax"></a>Sintaxe

*expressão* .Edit

*expressão* Uma variável que representa um objeto **Recordset**.

## <a name="remarks"></a>Comentários

Depois de usar o método **Edit**, as alterações feitas nos campos do registro atual são copiadas para o buffer de cópia. Após fazer as alterações desejadas no registro, use o método **[Update](recordset-update-method-dao.md)** para salvar as alterações.

O registro atual permanece atual após o uso de **Edit**.

> [!NOTE]
> Se você editar um registro e, em seguida, executar qualquer operação que mova para outro registro, mas sem utilizar primeiro **Update**, suas alterações serão perdidas sem aviso. Além disso, se você fechar recordset ou encerrar o procedimento que declara o **Recordset** ou o objeto pai **[Database](database-object-dao.md)** ou **[Connection](connection-object-dao.md)**, seu registro editado será descartado sem aviso.

Utilizar **Edit** produzirá um erro se:

- Não houver nenhum registro.

- O objeto **Connection**, **Database** ou **Recordset** tiver sido aberto como somente leitura.

- Nenhum campo no registro for atualizável.

- O **Database** ou o **Recordset** tiver sido aberto para ser utilizado exclusivamente por outro usuário (espaço de trabalho do Microsoft Access).

- Outro usuário bloqueou a página contendo seu registro (espaço de trabalho do Microsoft Access).

Em um espaço de trabalho do Microsoft Access, quando a configuração da propriedade [**LockEdits**](recordset-lockedits-property-dao.md) do objeto **Recordset** é **True** (bloqueado de forma pessimista) em um ambiente de vários usuários, o registro permanece bloqueado desde o momento em que **Edit** é usado até que a atualização seja concluída. Se a configuração da propriedade **LockEdits** for **False** (bloqueado de forma otimista), o registro será bloqueado e comparado ao registro pré-editado antes de ele ser atualizado no banco de dados. Se o registro foi alterado desde que você usou o método **Edit**, a operação **Update** falha com um erro de tempo de execução, se você usar **OpenRecordset** sem especificar **dbSeeChanges**. Por padrão, os bancos de dados ODBC e ISAM instalável conectados ao mecanismo de banco de dados do Microsoft Access sempre usam bloqueio otimista.

> [!NOTE]
> Para adicionar, editar ou excluir um registro, deve haver um índice exclusivo no registro, na fonte de dados de base. Se não houver, um erro "Permissão negada" ocorrerá na chamada do método **[AddNew](recordset-addnew-method-dao.md)**, **[Delete](fields-delete-method-dao.md)** ou **Edit** em um espaço de trabalho do Microsoft Access.

## <a name="example"></a>Exemplo

Este exemplo usa o método **Edit** para substituir os dados atuais pelo nome especificado. O procedimento EditName é exigido para que este procedimento seja executado.

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
