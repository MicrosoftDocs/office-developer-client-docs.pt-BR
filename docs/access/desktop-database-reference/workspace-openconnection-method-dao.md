---
title: Método Workspace.OpenConnection (DAO)
TOCTitle: OpenConnection Method
ms:assetid: 9d97f298-a2d5-3b91-2efd-57f06fbd4654
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198249(v=office.15)
ms:contentKeyID: 48546628
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 70bdded6c149aa7aff405c769ba4462a46c20dfd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308334"
---
# <a name="workspaceopenconnection-method-dao"></a>Método Workspace.OpenConnection (DAO)

**Aplica-se ao:** Access 2013, Office 2013

## <a name="syntax"></a>Sintaxe

*expressão* . OpenConnection(***Name***, ***Options***, ***ReadOnly***, ***Connect***)

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
<th><p>Necessária/opcional</p></th>
<th><p>Tipo de dados</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Name</em></p></td>
<td><p>Obrigatório</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Uma expressão em sequência. Consulte a discussão em Comentários.</p></td>
</tr>
<tr class="even">
<td><p><em>Opções</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variantes</strong></p></td>
<td><p>Define as várias opções para a conexão, como especificado em Comentários. Com base nessa valor, o gerenciador do driver ODBC solicita ao usuário informações de conexão, como o DSN (Nome da fonte de dados), o nome do usuário e a senha.</p></td>
</tr>
<tr class="odd">
<td><p><em>ReadOnly</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variantes</strong></p></td>
<td><p><strong>True</strong> se a conexão tiver que ser aberta para acesso somente leitura, e <strong>False</strong> se a conexão tiver que ser aberta para acesso de leitura/gravação (padrão).</p></td>
</tr>
<tr class="even">
<td><p><em>Connect</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variantes</strong></p></td>
<td><p>Uma cadeia de caracteres de conexão ODBC. Consulte a <strong><a href="connection-connect-property-dao.md">propriedade Connect</a></strong> para ver os elementos específicos e a sintaxe dessa cadeia de caracteres. Um &quot; ODBC anexado; &quot; é necessário.</p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a>Valor de retorno

Connection

## <a name="remarks"></a>Comentários

Use o método **OpenConnection** para estabelecer uma conexão com uma fonte de dados ODBC a partir de um espaço de trabalho ODBCDirect. O método **OpenConnection** é semelhante mas não igual a **OpenDatabase**. A principal diferença é que **OpenConnection** está disponível em um espaço de trabalho ODBCDirect.

Se você especificar um DSN (nome de fonte de dados) ODBC registrado no argumento connect, o argumento name pode ser qualquer cadeia de caracteres válida e também fornecerá a propriedade **Name** para o objeto **Connection.** Se um DSN válido não for incluído no argumento connect, o nome deverá se referir a um DSN ODBC válido, que também será a **propriedade Name.** Se nem o nome nem a conexão contiver um DSN válido, o gerenciador de driver ODBC poderá ser definido (por meio do argumento options) para solicitar ao usuário as informações de conexão necessárias. O DSN é fornecido pela solicitação e depois fornece a propriedade **Name**.

O argumento options determina se e quando solicitar que o usuário estabeleça a conexão e se a conexão será aberta de forma assíncrona ou não. Você pode usar uma das constantes a seguir.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constante</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>dbDriverNoPrompt</strong></p></td>
<td><p>O Gerenciador de Driver ODBC usa a cadeia de caracteres de conexão fornecida em <em>dbname</em> e <em>connect</em>. Se você não fornecer informações suficientes, ocorrerá um erro em tempo de execução.</p></td>
</tr>
<tr class="even">
<td><p><strong>dbDriverPrompt</strong></p></td>
<td><p>O Gerenciador de Driver ODBC exibe a caixa de diálogo <strong>Fontes de Dados ODBC</strong>, que exibe quaisquer informações relevantes fornecidas em <em>dbname</em> ou <em>connect</em>. A cadeia de caracteres de conexão é formada pelo DSN que o usuário seleciona por meio das caixas de diálogo. Se o usuário não especificar um DSN, o DSN padrão será usado.</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbDriverComplete</strong></p></td>
<td><p>Padrão. Se o argumento <em>connect</em> incluir todas as informações necessárias para estabelecer a conexão,  o Gerenciador de driver ODBC utilizará a sequência em <em>connect</em>. Caso contrário, ele se comportará da mesma forma como quando você especifica <strong>dbDriverPrompt</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>dbDriverCompleteRequired</strong></p></td>
<td><p>Essa opção se comporta como <strong>dbDriverComplete</strong> exceto pelo fato de que o driver ODBC desabilita as solicitações para qualquer informação não exigida para estabelecer a conexão.</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbRunAsync</strong></p></td>
<td><p>Execute o método de modo assíncrono. Essa constante pode ser usada com quaisquer outras constantes <em>options</em>.</p></td>
</tr>
</tbody>
</table>

<br/>

**OpenConnection** retorna um objeto **Connection** que contém informações sobre a conexão. O objeto **Connection** é semelhante ao objeto **[Database](database-object-dao.md)**. A principal diferença é que um objeto **Database** normalmente representa um banco de dados, embora ele possa ser usado para representar uma conexão com uma fonte de dados ODBC no espaço de trabalho do Microsoft Access.

## <a name="example"></a>Exemplo

Este exemplo usa o método **OpenConnection** com parâmetros diferentes para abrir três objetos **Connection** diferentes.

```vb 
Sub OpenConnectionX() 
 
 Dim wrkODBC As Workspace 
 Dim conPubs As Connection 
 Dim conPubs2 As Connection 
 Dim conPubs3 As Connection 
 Dim conLoop As Connection 
 
 ' Create ODBCDirect Workspace object. 
 Set wrkODBC = CreateWorkspace("NewODBCWorkspace", _ 
 "admin", "", dbUseODBC) 
 
 ' Open Connection object using supplied information in 
 ' the connect string. If this information were 
 ' insufficient, you could trap for an error rather than 
 ' go to an ODBC Driver Manager dialog box. 
 MsgBox "Opening Connection1..." 
 
 ' Note: The DSN referenced below must be set to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 Set conPubs = wrkODBC.OpenConnection("Connection1", _ 
 dbDriverNoPrompt, , _ 
 "ODBC;DATABASE=pubs;DSN=Publishers") 
 
 ' Open read-only Connection object based on information 
 ' you enter in the ODBC Driver Manager dialog box. 
 MsgBox "Opening Connection2..." 
 Set conPubs2 = wrkODBC.OpenConnection("Connection2", _ 
 dbDriverPrompt, True, "ODBC;DSN=Publishers;") 
 
 ' Open read-only Connection object by entering only the 
 ' missing information in the ODBC Driver Manager dialog 
 ' box. 
 MsgBox "Opening Connection3..." 
 Set conPubs3 = wrkODBC.OpenConnection("Connection3", _ 
 dbDriverCompleteRequired, True, _ 
 "ODBC;DATABASE=pubs;DSN=Publishers;") 
 
 ' Enumerate the Connections collection. 
 For Each conLoop In wrkODBC.Connections 
 Debug.Print "Connection properties for " & _ 
 conLoop.Name & ":" 
 
 With conLoop 
 ' Print property values by explicitly calling each 
 ' Property object; the Connection object does not 
 ' support a Properties collection. 
 Debug.Print " Connect = " & .Connect 
 ' Property actually returns a Database object. 
 Debug.Print " Database[.Name] = " & _ 
 .Database.Name 
 Debug.Print " Name = " & .Name 
 Debug.Print " QueryTimeout = " & .QueryTimeout 
 Debug.Print " RecordsAffected = " & _ 
 .RecordsAffected 
 Debug.Print " StillExecuting = " & _ 
 .StillExecuting 
 Debug.Print " Transactions = " & .Transactions 
 Debug.Print " Updatable = " & .Updatable 
 End With 
 
 Next conLoop 
 
 conPubs.Close 
 conPubs2.Close 
 conPubs3.Close 
 wrkODBC.Close 
 
End Sub 
 
```

<br/>

Este exemplo demonstra o objeto **Connection** e a coleção **Connections**, abrindo um objeto **Database** do Microsoft Access e dois objetos **Connection** ODBCDirect e listando as propriedades disponíveis para cada objeto.

```vb 
Sub ConnectionObjectX() 
 
 Dim wrkAcc as Workspace 
 Dim dbsNorthwind As Database 
 Dim wrkODBC As Workspace 
 Dim conPubs As Connection 
 Dim conPubs2 As Connection 
 Dim conLoop As Connection 
 Dim prpLoop As Property 
 
 ' Open Microsoft Access Database object. 
 Set wrkAcc = CreateWorkspace("NewWorkspace", _ 
 "admin", "", dbUseJet) 
 Set dbsNorthwind = wrkAcc.OpenDatabase("Northwind.mdb") 
 
 ' Create ODBCDirect Workspace object and open Connection 
 ' objects. 
 Set wrkODBC = CreateWorkspace("NewODBCWorkspace", _ 
 "admin", "", dbUseODBC) 
 
 ' Note: The DSNs referenced below must be configured to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 Set conPubs = wrkODBC.OpenConnection("Connection1", , , _ 
 "ODBC;DATABASE=pubs;DSN=Publishers") 
 
 Set conPubs2 = wrkODBC.OpenConnection("Connection2", , _ 
 True, "ODBC;DATABASE=pubs;DSN=Publishers") 
 
 Debug.Print "Database properties:" 
 
 With dbsNorthwind 
 ' Enumerate Properties collection of Database object. 
 For Each prpLoop In .Properties 
 On Error Resume Next 
 Debug.Print " " & prpLoop.Name & " = " & _ 
 prpLoop.Value 
 On Error GoTo 0 
 Next prpLoop 
 End With 
 
 ' Enumerate the Connections collection. 
 For Each conLoop In wrkODBC.Connections 
 Debug.Print "Connection properties for " & _ 
 conLoop.Name & ":" 
 
 With conLoop 
 ' Print property values by explicitly calling each 
 ' Property object; the Connection object does not 
 ' support a Properties collection. 
 Debug.Print " Connect = " & .Connect 
 ' Property actually returns a Database object. 
 Debug.Print " Database[.Name] = " & _ 
 .Database.Name 
 Debug.Print " Name = " & .Name 
 Debug.Print " QueryTimeout = " & .QueryTimeout 
 Debug.Print " RecordsAffected = " & _ 
 .RecordsAffected 
 Debug.Print " StillExecuting = " & _ 
 .StillExecuting 
 Debug.Print " Transactions = " & .Transactions 
 Debug.Print " Updatable = " & .Updatable 
 End With 
 
 Next conLoop 
 
 dbsNorthwind.Close 
 conPubs.Close 
 conPubs2.Close 
 wrkAcc.Close 
 wrkODBC.Close 
 
End Sub 
 
```

