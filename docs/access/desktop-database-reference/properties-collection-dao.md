---
title: Coleção Properties (DAO)
TOCTitle: Properties Collection
ms:assetid: cd07184a-a261-29c9-542f-bc2eff6f4af6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834455(v=office.15)
ms:contentKeyID: 48547753
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0f30ccd48ee5e4f4815be4d7e1ec6d94f237bc16
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25874283"
---
# <a name="properties-collection-dao"></a>Coleção Properties (DAO)


**Aplica-se a**: Access 2013, o Office 2013

Uma coleção **Properties** contém todos os objetos **[Property](property-object-dao.md)** de uma instância específica de um objeto.

## <a name="remarks"></a>Comentários

Todo objeto DAO, com exceção dos objetos **Connection** e **Error** contém uma coleção **Properties**, que tem certos objetos **Property** internos. Esses objetos **Property** (que geralmente são denominados apenas propriedades) caracterizam exclusivamente essa instância do objeto.

Além das propriedades internas, você também poderá criar e adicionar suas próprias propriedades definidas pelo usuário. Para adicionar uma propriedade definida pelo usuário a uma instância existente de um objeto, defina primeiramente suas características com o método **CreateProperty**, em seguida adicione-a à coleção com o método **Append**. Uma referência a um objeto **Property** definido pelo usuário que não tenha sido acrescentado ainda a uma coleção **Properties** causará um erro, bem como o acréscimo de um objeto **Property** definido pelo usuário a uma coleção **Properties** que contenha um objeto **Property** de mesmo nome.

É possível usar o método **Delete** para remover propriedades definidas pelo usuário da coleção **Properties**, mas não é possível remover propriedades internas.


> [!NOTE]
> <P>[!OBSERVAçãO] Um objeto <STRONG>Property</STRONG> definido pelo usuário está associado apenas à instância específica de um objeto. A propriedade não é definida para todas as instâncias de objetos do tipo selecionado.</P>



Para fazer referência a um objeto **Property** interno em uma coleção por seu número ordinal ou por sua configuração de propriedade **Name**, use uma das seguintes formas de sintaxe:

objeto. **Propriedades** (0)

objeto. **Propriedades** ("nome")

objeto. **Propriedades** \! \[nome\]

Para uma propriedade incorporada, você também pode usar esta sintaxe:

Object.Name


> [!NOTE]
> <P>Para uma propriedade definida pelo usuário, você deve usar o objeto completo. <STRONG>Propriedades</STRONG> sintaxe ("nome").</P>



Com as mesmas formas de sintaxe, você também pode referir-se à propriedade **Value** de um objeto **Property**. O contexto da referência determinará se você está se referindo ao objeto **Property** propriamente dito ou à propriedade **Value** do objeto **Property**.

## <a name="example"></a>Exemplo

Este exemplo cria uma propriedade definida pelo usuário para o banco de dados atual, define suas propriedades **Type** e **Value** e acrescenta-o à coleção **Properties** do banco de dados. Em seguida, são enumeradas no exemplo todas as propriedades do banco de dados.

```vb
    Sub PropertyX() 
     
     Dim dbsNorthwind As Database 
     Dim prpNew As Property 
     Dim prpLoop As Property 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     With dbsNorthwind 
     ' Create and append user-defined property. 
     Set prpNew = .CreateProperty() 
     prpNew.Name = "UserDefined" 
     prpNew.Type = dbText 
     prpNew.Value = "This is a user-defined property." 
     .Properties.Append prpNew 
     
     ' Enumerate all properties of current database. 
     Debug.Print "Properties of " & .Name 
     For Each prpLoop In .Properties 
     With prpLoop 
     Debug.Print " " & .Name 
     Debug.Print " Type: " & .Type 
     Debug.Print " Value: " & .Value 
     Debug.Print " Inherited: " & _ 
     .Inherited 
     End With 
     Next prpLoop 
     
     ' Delete new property because this is a 
     ' demonstration. 
     .Properties.Delete "UserDefined" 
     End With 
     
    End Sub 
```

<br/>

Este exemplo tenta definir o valor de uma propriedade definida pelo usuário. Se a propriedade não existir, ele usará o método **CreateProperty** para criar e definir o valor da nova propriedade. O procedimento SetProperty é exigido para a execução deste procedimento.

```vb
    Sub CreatePropertyX() 
     
     Dim dbsNorthwind As Database 
     Dim prpLoop As Property 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     ' Set the Archive property to True. 
     SetProperty dbsNorthwind, "Archive", True 
     
     With dbsNorthwind 
     Debug.Print "Properties of " & .Name 
     
     ' Enumerate Properties collection of the Northwind 
     ' database. 
     For Each prpLoop In .Properties 
     If prpLoop <> "" Then Debug.Print " " & _ 
     prpLoop.Name & " = " & prpLoop 
     Next prpLoop 
     
     ' Delete the new property since this is a 
     ' demonstration. 
     .Properties.Delete "Archive" 
     
     .Close 
     End With 
     
    End Sub 
     
    Sub SetProperty(dbsTemp As Database, strName As String, _ 
     booTemp As Boolean) 
     
     Dim prpNew As Property 
     Dim errLoop As Error 
     
     ' Attempt to set the specified property. 
     On Error GoTo Err_Property 
     dbsTemp.Properties("strName") = booTemp 
     On Error GoTo 0 
     
     Exit Sub 
     
    Err_Property: 
     
     ' Error 3270 means that the property was not found. 
     If DBEngine.Errors(0).Number = 3270 Then 
     ' Create property, set its value, and append it to the 
     ' Properties collection. 
     Set prpNew = dbsTemp.CreateProperty(strName, _ 
     dbBoolean, booTemp) 
     dbsTemp.Properties.Append prpNew 
     Resume Next 
     Else 
     ' If different error has occurred, display message. 
     For Each errLoop In DBEngine.Errors 
     MsgBox "Error number: " & errLoop.Number & vbCr & _ 
     errLoop.Description 
     Next errLoop 
     End 
     End If 
     
    End Sub
```
