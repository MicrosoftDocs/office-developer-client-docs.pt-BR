---
title: Método Database.CreateProperty (DAO)
TOCTitle: CreateProperty Method
ms:assetid: f2039be9-5fd8-f673-dfbf-0a71540cdc98
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836607(v=office.15)
ms:contentKeyID: 48548638
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f966e041a6d2aff773f6c3849c0846ef362d1142
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294971"
---
# <a name="databasecreateproperty-method-dao"></a>Método Database.CreateProperty (DAO)

**Aplica-se ao:** Access 2013, Office 2013

Cria um novo objeto **[Property](property-object-dao.md)** definido pelo usuário (apenas espaços de trabalho do Microsoft Access). .

## <a name="syntax"></a>Sintaxe

*expressão* . CreateProperty(***Name***, ***Type***, ***Value***, ***DDL***)

*expressão* Uma variável que representa um objeto do **Banco de dados**.

## <a name="parameters"></a>Parâmetros

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nome</p></th>
<th><p>Necessária/opcional</p></th>
<th><p>Tipo de dados</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Name</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variantes</strong></p></td>
<td><p>Uma <strong>String</strong> que denomina exclusivamente o novo objeto <strong>Property</strong>. Consulte a propriedade <strong>Name</strong> para obter detalhes sobre nomes válidos de <strong>Property</strong>.</p></td>
</tr>
<tr class="even">
<td><p><em>Type</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variantes</strong></p></td>
<td><p>Uma constante que define o tipo de dados do novo objeto <strong>Property</strong>. Consulte a propriedade <strong><a href="field-type-property-dao.md">Type</a></strong> para obter tipos de dados válidos.</p></td>
</tr>
<tr class="odd">
<td><p><em>Value</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variantes</strong></p></td>
<td><p>Um <strong>Variant</strong> que contém o valor inicial da propriedade. Consulte a <strong><a href="field-value-property-dao.md">propriedade Value</a></strong> para obter detalhes.</p></td>
</tr>
<tr class="even">
<td><p><em>DDL</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variantes</strong></p></td>
<td><p>Um <strong>Variant</strong> (subtipo <strong>Boolean</strong>) que indica se <strong>Property</strong> é ou não um objeto DDL. O padrão é False. Se DDL for True, os usuários não poderão alterar ou excluir esse objeto <strong>Property,</strong> a menos que tenham permissão dbSecWriteDef.</p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a>Valor de retorno

Propriedade

## <a name="remarks"></a>Comentários

Você pode criar um objeto **Property** definido pelo usuário na coleção **[Properties](properties-collection-dao.md)** de um objeto que é persistente.

Se você omitir uma ou mais das partes opcionais ao utilizar **CreateProperty**, poderá usar uma instruções de atribuição apropriada para definir ou redefinir a propriedade correspondente antes de acrescentar o novo objeto a uma coleção. Depois de acrescentar o objeto, você poderá alterar algumas, mas não todas, as configurações de propriedade. Consulte os tópicos de propriedade **Name**, **Type** e **Value** para obter mais detalhes.

Se o nome se referir a um objeto que já é membro da coleção, ocorrerá um erro em tempo de executar quando você usar o **[método Append.](fields-append-method-dao.md)**

Para remover um objeto **Property** definido pelo usuário da coleção, use o método **[Delete](fields-delete-method-dao.md)** na coleção **Properties**. Não é possível excluir propriedades internas.

> [!NOTE]
> Se você omitir o argumento DDL, ele será o padrão para False (não-DDL). Como nenhuma propriedade DDL correspondente está exposta, você deve excluir e recriar o objeto **Property** que deseja alterar de DDL para não-DDL.


## <a name="example"></a>Exemplo

Este exemplo tenta definir o valor de uma propriedade definida pelo usuário. Se a propriedade não existir, será usado o método **CreateProperty** para criar e definir o valor da nova propriedade. O procedimento SetProperty é exigido para a execução deste procedimento.

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
             If prpLoop <> "" Then Debug.Print "  " & _ 
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
