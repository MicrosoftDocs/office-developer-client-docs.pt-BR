---
title: Método Workspace.OpenDatabase (DAO)
TOCTitle: OpenDatabase Method
ms:assetid: dbb93908-ec3e-f3ee-c4ea-cca48340b4d3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835343(v=office.15)
ms:contentKeyID: 48548108
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: ca2ccb4183a59c2b579fd4375f26aa4fd539532f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302580"
---
# <a name="workspaceopendatabase-method-dao"></a>Método Workspace.OpenDatabase (DAO)

**Aplica-se ao**: Access 2013, Office 2013

Abre um banco de dados especificado em um objeto **[Workspace](workspace-object-dao.md)** e retorna uma referência ao objeto **[Database](database-object-dao.md)** que o representa.

## <a name="syntax"></a>Sintaxe

*expression* .OpenDatabase(***Name***, ***Options***, ***ReadOnly***, ***Connect***)

*expressão* Uma variável que representa um objeto **Workspace**.

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
<th><p>Necessário/opcional</p></th>
<th><p>Tipo de dados</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Name</em></p></td>
<td><p>Obrigatório</p></td>
<td><p><strong>String</strong></p></td>
<td><p>O nome de um arquivo de banco de dados existente no mecanismo de banco de dados do Microsoft Access ou o DSN (Nome da fonte de dados) de uma fonte de dados ODBC. Consulte a propriedade <strong><a href="connection-name-property-dao.md">Name</a></strong> para obter mais informações sobre a configuração desse valor.</p></td>
</tr>
<tr class="even">
<td><p><em>Opções</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Define as várias opções para o banco de dados, como especificado em Comentários.</p></td>
</tr>
<tr class="odd">
<td><p><em>ReadOnly</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p><strong>True</strong> se você quiser abrir o banco de dados com acesso somente leitura, ou <strong>False</strong> (padrão) se você quiser abrir o banco de dados com acesso de leitura/gravação.</p></td>
</tr>
<tr class="even">
<td><p><em>Connect</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Especifica várias informações de conexão, incluindo senhas.</p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a>Valor de retorno

Banco de dados

## <a name="remarks"></a>Comentários

Você pode usar os seguintes valores para o argumento de opções.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Setting</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Verdadeiro</strong></p></td>
<td><p>Abre o banco de dados no modo exclusivo.</p></td>
</tr>
<tr class="even">
<td><p><strong>Falso</strong></p></td>
<td><p>(Padrão) Abre o banco de dados no modo compartilhado.</p></td>
</tr>
</tbody>
</table>

<br/>

Quando você abre um banco de dados, ele é automaticamente adicionado à coleção **Databases**.

Algumas considerações se aplicam ao usar o dbname:

- Se ela se referir a um banco de dados que já foi aberto para acesso por outro usuário, ocorrerá um erro.

- Se ela não se referir a um banco de dados existente ou validar o nome da fonte de dados ODBC, ocorrerá um erro.

- Se for uma cadeia de caracteres de comprimento zero ("") e *conectar* for "ODBC" , será exibida uma caixa de diálogo listando todos os nomes de fonte de dados ODBC registrados para que o usuário possa selecionar um banco de dados.

Para fechar um banco de dados e, desse modo, remover o objeto **Database** da coleção **Databases**, use o método **[Close](connection-close-method-dao.md)** no objeto.

> [!NOTE]
> Ao acessar uma fonte de dados ODBC conectada ao mecanismo do banco de dados do Microsoft, você pode aprimorar o desempenho do aplicativo, abrindo um objeto **Database** conectado à fonte de dados ODBC, em vez de vincular objetos  **[TableDef](tabledef-object-dao.md)** individuais para especificar tabelas na fonte de dados ODBC.

## <a name="example"></a>Exemplo

Este exemplo usa o método **OpenDatabase** para abrir um banco de dados do Microsoft Access e dois bancos de dados ODBC conectados ao mecanismo de banco de dados do Microsoft Access.

```vb 
Sub OpenDatabaseX() 
 
 Dim wrkAcc As Workspace 
 Dim dbsNorthwind As Database 
 Dim dbsPubs As Database 
 Dim dbsPubs2 As Database 
 Dim dbsLoop As Database 
 Dim prpLoop As Property 
 
 ' Create Microsoft Access Workspace object. 
 Set wrkAcc = CreateWorkspace("", "admin", "", dbUseJet) 
 
 ' Open Database object from saved Microsoft Access database 
 ' for exclusive use. 
 MsgBox "Opening Northwind..." 
 Set dbsNorthwind = wrkAcc.OpenDatabase("Northwind.mdb", _ 
 True) 
 
 ' Open read-only Database object based on information in 
 ' the connect string. 
 MsgBox "Opening pubs..." 
 
 ' Note: The DSN referenced below must be set to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 Set dbsPubs = wrkAcc.OpenDatabase("Publishers", _ 
 dbDriverNoPrompt, True, _ 
 "ODBC;DATABASE=pubs;DSN=Publishers") 
 
 ' Open read-only Database object by entering only the 
 ' missing information in the ODBC Driver Manager dialog 
 ' box. 
 MsgBox "Opening second copy of pubs..." 
 Set dbsPubs2 = wrkAcc.OpenDatabase("Publishers", _ 
 dbDriverCompleteRequired, True, _ 
 "ODBC;DATABASE=pubs;DSN=Publishers;") 
 
 ' Enumerate the Databases collection. 
 For Each dbsLoop In wrkAcc.Databases 
 Debug.Print "Database properties for " & _ 
 dbsLoop.Name & ":" 
 
 On Error Resume Next 
 ' Enumerate the Properties collection of each Database 
 ' object. 
 For Each prpLoop In dbsLoop.Properties 
 If prpLoop.Name = "Connection" Then 
 ' Property actually returns a Connection object. 
 Debug.Print " Connection[.Name] = " & _ 
 dbsLoop.Connection.Name 
 Else 
 Debug.Print " " & prpLoop.Name & " = " & _ 
 prpLoop 
 End If 
 Next prpLoop 
 On Error GoTo 0 
 
 Next dbsLoop 
 
 dbsNorthwind.Close 
 dbsPubs.Close 
 dbsPubs2.Close 
 wrkAcc.Close 
 
End Sub 
 
```

