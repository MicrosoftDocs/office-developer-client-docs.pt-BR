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
ms.openlocfilehash: ce7d907db9d16ead7cfa355ecf4f9e87e04f8095
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/01/2018
ms.locfileid: "25891293"
---
# <a name="recordsetaddnew-method-dao"></a>Método Recordset.AddNew (DAO)


**Aplica-se a**: Access 2013, o Office 2013

Cria um novo registro para um objeto **[Recordset](recordset-object-dao.md)** atualizável.

## <a name="syntax"></a>Sintaxe

*expressão* . AddNew

*expressão* Uma variável que representa um objeto **Recordset** .

## <a name="remarks"></a>Comentários

Use o método **AddNew** para criar e adicionar um novo registro no objeto **Recordset** com o nome do conjunto de registros. Este método define os campos como os valores padrão e, se nenhum valor padrão for especificado, ele definirá os campos como Nulo (os valores padrão especificados para um **Recordset** do tipo tabela).

Depois de modificar o novo registro, use o método **[Update](recordset-update-method-dao.md)** para salvar as alterações e adicionar o registro ao **Recordset**. Não haverá alterações no banco de dados até você usar o método **Update**.


> [!NOTE]
> <P>[!OBSERVAçãO] Se você emitir um <STRONG>AddNew</STRONG> e então executar qualquer operação que mova para outro registro, mas sem usar <STRONG>Update</STRONG>, suas alterações serão perdidas sem aviso. Além disso, se você fechar o <STRONG>Recordset</STRONG> ou encerrar o procedimento que declara o <STRONG>Recordset</STRONG> ou seu objeto <STRONG><A href="database-object-dao.md">Database</A></STRONG>, o novo registro será descartado sem aviso.</P>




> [!NOTE]
> <P>[!OBSERVAçãO] Quando você usa <STRONG>AddNew</STRONG> em um espaço de trabalho do Microsoft Access e o mecanismo de banco de dados tem de criar uma nova página para conter o registro atual, o bloqueio de página será pessimista. Se o novo registro se ajustar a uma página existente, o bloqueio de página será otimista.</P>



Se você não tiver se movido para o último registro do seu **Recordset**, os registros adicionados a tabelas base por outros processos poderão ser incluídos caso tenham sido posicionados além do registro atual. No entanto, se você adicionar um registro ao seu próprio **Recordset**, o registro ficará visível no **Recordset** e será incluído na tabela subjacente onde se tornará visível para todos os objetos novos do **Recordset**.

A posição do novo registro depende do tipo de **Recordset**.

  - Em um objeto **Recordset** do tipo dynaset, os registros são inseridos no final do **Recordset**, independentemente de qualquer regra de classificação ou de ordenação em vigor quando o **Recordset** tiver sido aberto.

  - Em um objeto **Recordset** do tipo tabela cuja propriedade **[Index](recordset-index-property-dao.md)** tenha sido definida, os registros serão retornados no local apropriado na ordem de classificação. Se você não tiver definido a propriedade **Index**, os novos registros serão retornados no final do **Recordset**.

O registro que era o atual quando você usou o **AddNew** permanece atual. Se você quiser tornar o novo registro atual, poderá definir a propriedade **[Bookmark](recordset-bookmark-property-dao.md)** como o indicador identificado pela configuração da propriedade **[LastModified](recordset-lastmodified-property-dao.md)**.


> [!NOTE]
> <P>[!OBSERVAçãO] Para adicionar, editar ou excluir um registro, deve haver um índice exclusivo no registro na fonte de dados subjacente. Caso contrário, ocorrerá um erro "Permissão negada" na chamada ao método <STRONG>AddNew</STRONG>, <STRONG>Delete</STRONG> ou <STRONG>Edit</STRONG> em um espaço de trabalho do Microsoft Access.</P>



## <a name="example"></a>Exemplo

Este exemplo usa o método **AddNew** para criar um novo registro com o nome especificado. A função AddName é necessária para executar esse procedimento.

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
