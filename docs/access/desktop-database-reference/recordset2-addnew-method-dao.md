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
# <a name="recordset2addnew-method-dao"></a>Método Recordset2.AddNew (DAO)


**Aplica-se a**: Access 2013, o Office 2013
 

Cria um novo registro para um objeto **Recordset2** atualizável.

## <a name="syntax"></a>Sintaxe

*expressão* . AddNew

*expressão* Uma variável que representa um objeto **Recordset2** .

## <a name="remarks"></a>Comentários

Use o método **AddNew** para criar e adicionar um novo registro ao objeto **Recordset2** denominado por recordset. Este método define valores padrão para os campos e, se nenhum valor padrão estiver especificado, ele definirá os campos como nulos (os valores padrão especificados para um **Recordset2** do tipo tabela).

Depois de modificar o novo registro, use o método **[Update](recordset2-update-method-dao.md)** para salvar as alterações e adicionar o registro ao **Recordset2**. Nenhuma alteração ocorrerá no banco de dados até você usar o método **Update**.


> [!NOTE]
> <P>[!OBSERVAçãO] Se você emitir um <STRONG>AddNew</STRONG> e, em seguida, executar qualquer operação que mova para outro registro, mas sem usar <STRONG>Update</STRONG>, suas alterações serão perdidas sem aviso. Além disso, se você fechar o <STRONG>Recordset2</STRONG> ou concluir o procedimento que declara o <STRONG>Recordset2</STRONG> ou seu objeto <STRONG><A href="database-object-dao.md">Database</A></STRONG>, o novo registro será descartado sem aviso.</P>




> [!NOTE]
> <P>[!OBSERVAçãO] Quando você usa <STRONG>AddNew</STRONG> em um espaço de trabalho do Microsoft Access e o mecanismo de banco de dados tem que criar uma nova página para o registro atual, o bloqueio de página é pessimista. Se o novo registro couber em uma página existente, o bloqueio de página será otimista.</P>



Se você não tiver movido para o último registro do seu **Recordset2**, os registros adicionados a tabelas base por outros processos poderão ser incluídos se estiverem posicionados além do registro atual. Se você adicionar um registro a seu próprio **Recordset2**, no entanto, o registro estará visível no **Recordset2** e incluído na tabela subjacente onde se tornará visível para quaisquer novos objetos **Recordset2**.

A posição do novo registro depende do tipo do **Recordset2**:

  - Em um objeto **Recordset2** do tipo dynaset, registros são inseridos no fim do **Recordset**, independentemente de qualquer regra de classificação ou ordenação aplicada quando o **Recordset** foi aberto.

  - Em um objeto **Recordset2** do tipo tabela cuja propriedade **[Index](recordset2-index-property-dao.md)** tiver sido definida, os registros serão retornados em seu próprio lugar na ordem de classificação. Se você não tiver definido a propriedade **Index**, novos registros serão retornados no fim do **Recordset**.

O registro que era o atual antes de você usar o **AddNew** continuará sendo o atual. Se desejar tornar o novo registro atual, você poderá definir a propriedade **[Bookmark](recordset2-bookmark-property-dao.md)** para o indicador identificado pela configuração da propriedade **[LastModified](recordset2-lastmodified-property-dao.md)**.


> [!NOTE]
> <P>[!OBSERVAçãO] Para adicionar, editar ou excluir um registro, deve haver um índice exclusivo no registro na fonte de dados subjacente. Caso contrário, ocorrerá um erro "Permissão negada" na chamada ao método <STRONG>AddNew</STRONG>, <STRONG>Delete</STRONG> ou <STRONG>Edit</STRONG> em um espaço de trabalho do Microsoft Access.</P>



## <a name="example"></a>Exemplo

Este exemplo usa o método **AddNew** para criar um novo registro com o nome especificado. A função AddName é necessária para executar esse procedimento.

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
