---
title: Objeto container (DAO)
TOCTitle: Container Object
ms:assetid: 22e487cd-e966-fe68-fff3-c680b460cbeb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191764(v=office.15)
ms:contentKeyID: 48543720
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ba9284e0d62c99ab9bcb631b29587e16a3d76bce
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25919511"
---
# <a name="container-object-dao"></a>Objeto container (DAO)

**Aplica-se a**: Access 2013, o Office 2013

Um objeto **Container** agrupa tipos semelhantes de objetos **Document**.

## <a name="remarks"></a>Comentários

Cada objeto **Database** tem uma coleção **Containers** que consiste em objetos **Container** incorporados. Os aplicativos podem definir seus próprios tipos de documentos e contêineres correspondentes (apenas bancos de dados do mecanismo de banco de dados do Microsoft Access); entretanto, esses objetos nem sempre são aceitos no DAO.

Alguns desses objetos **Container** são definidos pelo mecanismo de banco de dados do Microsoft Access enquanto outros podem ser definidos por outros aplicativos. A tabela a seguir lista o nome de cada objeto **Container** definido pelo mecanismo de banco de dados do Microsoft Access e o tipo de informações que ele contém.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nome do contêiner</p></th>
<th><p>Contém informações sobre</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Databases</p></td>
<td><p>Bancos de dados salvos</p></td>
</tr>
<tr class="even">
<td><p>Tables</p></td>
<td><p>Tabelas e consultas salvas</p></td>
</tr>
<tr class="odd">
<td><p>Relations</p></td>
<td><p>Relações salvas</p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> [!OBSERVAçãO] Não confunda os objetos **Container** listados na tabela anterior com as coleções de mesmo nome. O objeto **Container** do banco de dados se refere a todos os objetos salvos do banco de dados, mas a coleção **Databases** se refere apenas aos objetos do banco de dados que estão abertos em um determinado espaço de trabalho.

Cada objeto **Container** tem uma coleção **Documents** que contém objetos **Document** que descrevem instâncias de objetos incorporados do tipo especificado pelo **Container**. Você normalmente usa um objeto **Container** como um link intermediário para as informações no objeto **Document**. Você também pode usar a coleção **Containers** para definir segurança em todos os objetos **Document** de um determinado tipo.

Com um objeto **Container** existente, você pode:

- Usar a propriedade **Name** para retornar o nome predefinido do objeto **Container**.

- Usar a propriedade **Owner** para definir ou retornar o proprietário do objeto **Container**. Para definir a propriedade **Owner**, você deve ter permissão de gravação no objeto **Container** e definir a propriedade para o nome de um objeto **User** ou **Group** existente.

- Usar as propriedades **Permissions** e **UserName** para definir as permissões de acesso para o objeto **Container**; qualquer objeto **Document** criado na coleção **Documents** de um objeto **Container** herda essas configurações de permissão de acesso.

Como os objetos **Container** são incorporados, você não pode criar novos objetos **Container** nem excluir os existentes.

Para referir-se a um objeto **Container** de uma coleção pelo número ordinal ou pela configuração da propriedade **Name**, use qualquer uma das formas de sintaxe a seguir:

- **Containers**(0)

- **Contêineres** ("*nome*")

- **Contêineres**\!\[*nome*\]

## <a name="example"></a>Exemplo

Este exemplo enumera a coleção **Containers** do banco de dados Northwind e a coleção **Properties** de cada objeto **Container** na coleção.

```vb
    Sub ContainerObjectX() 
     
     Dim dbsNorthwind As Database 
     Dim ctrLoop As Container 
     Dim prpLoop As Property 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     With dbsNorthwind 
     
     ' Enumerate Containers collection. 
     For Each ctrLoop In .Containers 
     Debug.Print "Properties of " & ctrLoop.Name _ 
     & " container" 
     
     ' Enumerate Properties collection of each 
     ' Container object. 
     For Each prpLoop In ctrLoop.Properties 
     Debug.Print " " & prpLoop.Name _ 
     & " = " prpLoop 
     Next prpLoop 
     
     Next ctrLoop 
     
     .Close 
     End With 
     
    End Sub
```
