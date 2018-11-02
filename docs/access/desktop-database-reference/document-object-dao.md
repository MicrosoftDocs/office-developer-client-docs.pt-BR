---
title: Objeto Document (DAO)
TOCTitle: Document Object
ms:assetid: b51d4545-b157-4c7c-fdbe-16a25afffdb3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822082(v=office.15)
ms:contentKeyID: 48547247
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 17dfd7d1a6f5a0c7ec6bd985d75d201202a71ff7
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25922311"
---
# <a name="document-object-dao"></a>Objeto Document (DAO)


**Aplica-se a**: Access 2013, o Office 2013

O objeto **Document** inclui informações sobre uma instância de um objeto. O objeto pode ser um banco de dados, uma tabela, uma consulta ou uma relação salva (apenas bancos de dados do mecanismo de banco de dados do Microsoft Access).

## <a name="remarks"></a>Comentários

Cada objeto **Container** tem uma coleção **Documents** que contém objetos **Document** que descrevem instâncias de objetos incorporados do tipo especificado pelo **Container**. A tabela a seguir lista o tipo de objeto que cada **Document** descreve, o nome desse objeto **Container** e o tipo de informações que **Document** contém.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Document</p></th>
<th><p>Container</p></th>
<th><p>Contém informações sobre</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Banco de dados</p></td>
<td><p>Databases</p></td>
<td><p>Banco de dados salvo</p></td>
</tr>
<tr class="even">
<td><p>Tabela ou consulta</p></td>
<td><p>Tables</p></td>
<td><p>Tabela ou consulta salva</p></td>
</tr>
<tr class="odd">
<td><p>Relação</p></td>
<td><p>Relations</p></td>
<td><p>Relações salvas</p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> [!OBSERVAçãO] Não confunda os objetos **Container** listados na tabela anterior com as coleções de mesmo nome. O objeto **Container** do banco de dados se refere a todos os objetos salvos do banco de dados, mas a coleção **Databases** se refere apenas aos objetos do banco de dados que estão abertos em um determinado espaço de trabalho.



Com um objeto **Document**, você pode:

  - Usar a propriedade **Name** para retornar o nome que um usuário ou mecanismo de banco de dados do Microsoft Access deu ao objeto quando ele foi criado.

  - Usar a propriedade **Container** para retornar o nome do objeto **Container** que contém o objeto **Document**.

  - Usar a propriedade **Owner** para definir ou retornar o proprietário do objeto. Para definir a propriedade **Owner**, você deve ter permissão de gravação no objeto **Document** e definir a propriedade para o nome de um objeto **User** ou **Group** existente.

  - Usar as propriedades **UserName** ou **Permissions** para definir ou retornar as permissões de acesso de um usuário ou grupo para o objeto. Para definir essas propriedades, você deve ter permissão de gravação no objeto **Document** e definir a propriedade **UserName** para o nome de um objeto **User** ou **Group** existente.

  - Usar as propriedades **DateCreated** e **LastUpdated** para retornar a data e a hora em que o objeto **Document** foi criado e modificado pela última vez.

Como um objeto **Document** corresponde a um objeto existente, você não poderá criar novos objetos **Document** nem excluir objetos existentes. Para referir-se a um objeto **Document** de uma coleção pelo número ordinal ou pela configuração da propriedade **Name**, use qualquer uma das formas de sintaxe a seguir:

  - **Documents**(0)

  - **Documentos** ("*nome*")

  - **Documentos**\!\[*nome*\]

## <a name="example"></a>Exemplo

Este exemplo enumera a coleção **Documents** do contêineer Tables e enumera a coleção **Properties** do primeiro objeto **Document** na coleção.

```vb 
Sub DocumentX() 
 
 Dim dbsNorthwind As Database 
 Dim docLoop As Document 
 Dim prpLoop As Property 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 
 With dbsNorthwind.Containers!Tables 
 Debug.Print "Documents in " & .Name & " container" 
 ' Enumerate the Documents collection of the Tables 
 ' container. 
 For Each docLoop In .Documents 
 Debug.Print " " & docLoop.Name 
 Next docLoop 
 With .Documents(0) 
 ' Enumerate the Properties collection of the first. 
 ' Document object of the Tables container. 
 Debug.Print "Properties of " & .Name & " document" 
 On Error Resume Next 
 For Each prpLoop In .Properties 
 Debug.Print " " & prpLoop.Name & " = " & _ 
 prpLoop 
 Next prpLoop 
 On Error GoTo 0 
 End With 
 End With 
 
 dbsNorthwind.Close 
 
End Sub 
 
```

Este exemplo usa as propriedades **Owner** e **SystemDB** para mostrar os proprietários de uma variedade dos objetos **Document**.

```vb 
Sub OwnerX() 
 
 ' Ensure that the Microsoft Access workgroup file is 
 ' available. 
 DBEngine.SystemDB = "system.mdw" 
 
 Dim dbsNorthwind As Database 
 Dim ctrLoop As Container 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 
 With dbsNorthwind 
 Debug.Print "Document owners:" 
 ' Enumerate Containers collection and show the owner 
 ' of the first Document in each container's Documents 
 ' collection. 
 For Each ctrLoop In .Containers 
 With ctrLoop 
 Debug.Print " [" & .Documents(0).Name & _ 
 "] in [" & .Name & _ 
 "] container owned by [" & _ 
 .Documents(0).Owner & "]" 
 End With 
 Next ctrLoop 
 
 .Close 
 End With 
 
End Sub 
 
```

