---
title: Propriedade Field2.DefaultValue (DAO)
TOCTitle: DefaultValue Property
ms:assetid: 709c9580-520e-46ce-7d70-e409872184bb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195744(v=office.15)
ms:contentKeyID: 48545563
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053121
f1_categories:
- Office.Version=v15
ms.openlocfilehash: cff7a319130786cfdab26546d49f83da5769c5f6
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464204"
---
# <a name="field2defaultvalue-property-dao"></a>Propriedade Field2.DefaultValue (DAO)


**Aplica-se a**: Access 2013 | Office 2013


Define ou retorna o valor padrão de um objeto **Field2**. Para um objeto **Field2** ainda não acrescentado à coleção **[Fields](fields-collection-dao.md)**, essa propriedade é de leitura/gravação (apenas espaços de trabalho do Microsoft Access).

## <a name="syntax"></a>Sintaxe

*expressão* . DefaultValue

*expressão* Uma variável que representa um objeto **Field2** .

## <a name="remarks"></a>Comentários

A configuração ou o valor de retorno é um tipo de dados **String** que pode conter no máximo 255 caracteres. Ele pode conter texto ou uma expressão. Se a configuração da propriedade for uma expressão, ela não poderá conter funções definidas pelo usuário, funções agregadas do mecanismo de banco de dados do Microsoft Access SQL ou referência a consultas, formulários ou outros objetos **Field2**.


> [!NOTE]
> <P>[!OBSERVAçãO] Você também pode definir a propriedade <STRONG>DefaultValue</STRONG> de um objeto <STRONG>Field2</STRONG> em um objeto <STRONG>TableDef</STRONG> para um valor especial chamado "GenUniqueID( )". Isso faz com que um número aleatório seja atribuído a esse campo sempre que um novo registro é adicionado ou criado, fornecendo a cada registro um identificador exclusivo. A propriedade <STRONG>Type</STRONG> do campo de ver <STRONG>Long</STRONG>.</P>



A disponibilidade da propriedade **DefaultValue** depende do objeto que contém a coleção **Fields**, conforme mostrado na tabela a seguir.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Se a coleção Fields pertencer a</p></th>
<th><p>DefaultValue será</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Objeto Index</p></td>
<td><p>Sem suporte</p></td>
</tr>
<tr class="even">
<td><p>Objeto QueryDef</p></td>
<td><p>Somente leitura</p></td>
</tr>
<tr class="odd">
<td><p>Objeto Recordset</p></td>
<td><p>Somente leitura</p></td>
</tr>
<tr class="even">
<td><p>Objeto Relation</p></td>
<td><p>Sem suporte</p></td>
</tr>
<tr class="odd">
<td><p>Objeto TableDef</p></td>
<td><p>Leitura/gravação</p></td>
</tr>
</tbody>
</table>


Quando um novo registro é criado, a configuração da propriedade **DefaultValue** é automaticamente inserida como o valor para o campo. Você pode alterar o valor de campo definindo sua propriedade **Value**.

A propriedade **DefaultValue** não se aplica aos campos **AutoNumber** e **Long Binary**.

## <a name="example"></a>Exemplo

Este exemplo usa a propriedade **DefaultValue** para alertar o usuário de um valor normal de campo durante a solicitação de entrada. Além disso, ele demonstra como os novos registros serão preenchidos utilizando o **DefaultValue** na ausência de qualquer outra entrada. A função DefaultPrompt é exigida para que este procedimento seja executado.

```vb
    Sub DefaultValueX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim strOldDefault As String 
     Dim rstEmployees As Recordset 
     Dim strMessage As String 
     Dim strCode As String 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind.TableDefs!Employees 
     
     ' Store original DefaultValue information and set the 
     ' property to a new value. 
     strOldDefault = _ 
     tdfEmployees.Fields!PostalCode.DefaultValue 
     tdfEmployees.Fields!PostalCode.DefaultValue = "98052" 
     
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees", _ 
     dbOpenDynaset) 
     
     With rstEmployees 
     ' Add a new record to the Recordset. 
     .AddNew 
     !FirstName = "Bruce" 
     !LastName = "Oberg" 
     
     ' Get user input. If user enters something, the field 
     ' will be filled with that data; otherwise, it will be 
     ' filled with the DefaultValue information. 
     strMessage = "Enter postal code for " & vbCr & _ 
     !FirstName & " " & !LastName & ":" 
     strCode = DefaultPrompt(strMessage, !PostalCode) 
     If strCode <> "" Then !PostalCode = strCode 
     .Update 
     
     ' Go to new record and print information. 
     .Bookmark = .LastModified 
     Debug.Print " FirstName = " & !FirstName 
     Debug.Print " LastName = " & !LastName 
     Debug.Print " PostalCode = " & !PostalCode 
     
     ' Delete new record because this is a demonstration. 
     .Delete 
     .Close 
     End With 
     
     ' Restore original DefaultValue property because this is a 
     ' demonstration. 
     tdfEmployees.Fields!PostalCode.DefaultValue = _ 
     strOldDefault 
     
     dbsNorthwind.Close 
     
    End Sub 
     
    Function DefaultPrompt(strPrompt As String, _ 
     fldTemp As Field2) As String 
     
     Dim strFullPrompt As String 
     
     ' Ask user for new DefaultValue setting for the specified 
     ' Field object. 
     strFullPrompt = strPrompt & vbCr & _ 
     "[Default = " & fldTemp.DefaultValue & _ 
     ", Cancel - use default]" 
     DefaultPrompt = InputBox(strFullPrompt) 
     
    End Function
```
