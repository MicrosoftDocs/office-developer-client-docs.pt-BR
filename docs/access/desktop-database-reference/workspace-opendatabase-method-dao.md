---
title: Método Workspace.OpenDatabase (DAO)
TOCTitle: OpenDatabase Method
ms:assetid: dbb93908-ec3e-f3ee-c4ea-cca48340b4d3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835343(v=office.15)
ms:contentKeyID: 48548108
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4c4f799d9e0e3ea2ffddbf981adf9332cca672ee
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25997284"
---
# <a name="workspaceopendatabase-method-dao"></a><span data-ttu-id="3452e-102">Método Workspace.OpenDatabase (DAO)</span><span class="sxs-lookup"><span data-stu-id="3452e-102">Workspace.OpenDatabase method (DAO)</span></span>

<span data-ttu-id="3452e-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="3452e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3452e-104">Abre um banco de dados especificado em um objeto **[Workspace](workspace-object-dao.md)** e retorna uma referência ao objeto **[Database](database-object-dao.md)** que o representa.</span><span class="sxs-lookup"><span data-stu-id="3452e-104">Opens a specified database in a **[Workspace](workspace-object-dao.md)** object and returns a reference to the **[Database](database-object-dao.md)** object that represents it.</span></span>

## <a name="syntax"></a><span data-ttu-id="3452e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3452e-105">Syntax</span></span>

<span data-ttu-id="3452e-106">*expressão* . OpenDatabase (***nome***, ***Opções***, ***ReadOnly***, ***Conecte-se***)</span><span class="sxs-lookup"><span data-stu-id="3452e-106">*expression* .OpenDatabase(***Name***, ***Options***, ***ReadOnly***, ***Connect***)</span></span>

<span data-ttu-id="3452e-107">*expressão* Uma variável que representa um objeto **Workspace** .</span><span class="sxs-lookup"><span data-stu-id="3452e-107">*expression* A variable that represents a **Workspace** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="3452e-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3452e-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3452e-109">Nome</span><span class="sxs-lookup"><span data-stu-id="3452e-109">Name</span></span></p></th>
<th><p><span data-ttu-id="3452e-110">Obrigatório/opcional</span><span class="sxs-lookup"><span data-stu-id="3452e-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="3452e-111">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="3452e-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="3452e-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="3452e-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3452e-113"><em>Nome</em></span><span class="sxs-lookup"><span data-stu-id="3452e-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="3452e-114">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="3452e-114">Required</span></span></p></td>
<td><p><span data-ttu-id="3452e-115"><strong>CadeiaDeCaracteres</strong></span><span class="sxs-lookup"><span data-stu-id="3452e-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="3452e-p101">O nome de um arquivo de banco de dados existente no mecanismo de banco de dados do Microsoft Access ou o DSN (Nome da fonte de dados) de uma fonte de dados ODBC. Consulte a propriedade <strong><a href="connection-name-property-dao.md">Name</a></strong> para obter mais informações sobre a configuração desse valor.  </span><span class="sxs-lookup"><span data-stu-id="3452e-p101">the name of an existing Microsoft Access database engine database file, or the data source name (DSN) of an ODBC data source. See the <strong><a href="connection-name-property-dao.md">Name</a></strong> property for more information about setting this value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3452e-118"><em>Options</em></span><span class="sxs-lookup"><span data-stu-id="3452e-118"><em>Options</em></span></span></p></td>
<td><p><span data-ttu-id="3452e-119">Opcional</span><span class="sxs-lookup"><span data-stu-id="3452e-119">Optional</span></span></p></td>
<td><p><span data-ttu-id="3452e-120"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="3452e-120"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="3452e-121">Define as várias opções para o banco de dados, como especificado em Comentários.</span><span class="sxs-lookup"><span data-stu-id="3452e-121">Sets various options for the database, as specified in Remarks.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3452e-122"><em>ReadOnly</em></span><span class="sxs-lookup"><span data-stu-id="3452e-122"><em>ReadOnly</em></span></span></p></td>
<td><p><span data-ttu-id="3452e-123">Opcional</span><span class="sxs-lookup"><span data-stu-id="3452e-123">Optional</span></span></p></td>
<td><p><span data-ttu-id="3452e-124"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="3452e-124"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="3452e-125"><strong>True</strong> se você quiser abrir o banco de dados com acesso somente leitura, ou <strong>False</strong> (padrão) se você quiser abrir o banco de dados com acesso de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="3452e-125"><strong>True</strong> if you want to open the database with read-only access, or <strong>False</strong> (default) if you want to open the database with read/write access.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3452e-126"><em>Connect</em></span><span class="sxs-lookup"><span data-stu-id="3452e-126"><em>Connect</em></span></span></p></td>
<td><p><span data-ttu-id="3452e-127">Opcional</span><span class="sxs-lookup"><span data-stu-id="3452e-127">Optional</span></span></p></td>
<td><p><span data-ttu-id="3452e-128"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="3452e-128"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="3452e-129">Especifica várias informações de conexão, incluindo senhas.</span><span class="sxs-lookup"><span data-stu-id="3452e-129">Specifies various connection information, including passwords.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="3452e-130">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="3452e-130">Return value</span></span>

<span data-ttu-id="3452e-131">Banco de dados</span><span class="sxs-lookup"><span data-stu-id="3452e-131">Database</span></span>

## <a name="remarks"></a><span data-ttu-id="3452e-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="3452e-132">Remarks</span></span>

<span data-ttu-id="3452e-133">Você pode usar os valores a seguir para o argumento options.</span><span class="sxs-lookup"><span data-stu-id="3452e-133">You can use the following values for the options argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3452e-134">Configuração</span><span class="sxs-lookup"><span data-stu-id="3452e-134">Setting</span></span></p></th>
<th><p><span data-ttu-id="3452e-135">Descrição</span><span class="sxs-lookup"><span data-stu-id="3452e-135">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3452e-136"><strong>True</strong></span><span class="sxs-lookup"><span data-stu-id="3452e-136"><strong>True</strong></span></span></p></td>
<td><p><span data-ttu-id="3452e-137">Abre o banco de dados no modo exclusivo.</span><span class="sxs-lookup"><span data-stu-id="3452e-137">Opens the database in exclusive mode.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3452e-138"><strong>False</strong></span><span class="sxs-lookup"><span data-stu-id="3452e-138"><strong>False</strong></span></span></p></td>
<td><p><span data-ttu-id="3452e-139">(Padrão) Abre o banco de dados no modo compartilhado.</span><span class="sxs-lookup"><span data-stu-id="3452e-139">(Default) Opens the database in shared mode.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="3452e-140">Quando você abre um banco de dados, ele é automaticamente adicionado à coleção **Databases**.</span><span class="sxs-lookup"><span data-stu-id="3452e-140">When you open a database, it is automatically added to the **Databases** collection.</span></span>

<span data-ttu-id="3452e-141">Algumas considerações se aplicam quando se usa dbname:</span><span class="sxs-lookup"><span data-stu-id="3452e-141">Some considerations apply when you use dbname:</span></span>

- <span data-ttu-id="3452e-142">Se ela se referir a um banco de dados que já foi aberto para acesso por outro usuário, ocorrerá um erro.</span><span class="sxs-lookup"><span data-stu-id="3452e-142">If it refers to a database that is already open for access by another user, an error occurs.</span></span>

- <span data-ttu-id="3452e-143">Se ela não se referir a um banco de dados existente ou validar o nome da fonte de dados ODBC, ocorrerá um erro.</span><span class="sxs-lookup"><span data-stu-id="3452e-143">If it doesn't refer to an existing database or valid ODBC data source name, an error occurs.</span></span>

- <span data-ttu-id="3452e-144">Se for uma cadeia de caracteres de comprimento zero ("") e *Conecte-se* for "ODBC;", uma caixa de diálogo listando todos os registrados nomes de fonte de dados ODBC é exibida para que o usuário possa selecionar um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="3452e-144">If it's a zero-length string ("") and *connect* is "ODBC;" , a dialog box listing all registered ODBC data source names is displayed so the user can select a database.</span></span>

<span data-ttu-id="3452e-145">Para fechar um banco de dados e, desse modo, remover o objeto **Database** da coleção **Databases**, use o método **[Close](connection-close-method-dao.md)** no objeto.</span><span class="sxs-lookup"><span data-stu-id="3452e-145">To close a database, and thus remove the **Database** object from the **Databases** collection, use the **[Close](connection-close-method-dao.md)** method on the object.</span></span>

> [!NOTE]
> <span data-ttu-id="3452e-146">[!OBSERVAçãO] Ao acessar uma fonte de dados ODBC conectada ao mecanismo do banco de dados do Microsoft, você pode aprimorar o desempenho do aplicativo, abrindo um objeto **Database** conectado à fonte de dados ODBC, em vez de vincular objetos **[TableDef](tabledef-object-dao.md)** individuais para especificar tabelas na fonte de dados ODBC.</span><span class="sxs-lookup"><span data-stu-id="3452e-146">When you access a Microsoft access database engine-connected ODBC data source, you can improve your application's performance by opening a **Database** object connected to the ODBC data source, rather than by linking individual **[TableDef](tabledef-object-dao.md)** objects to specific tables in the ODBC data source.</span></span>

## <a name="example"></a><span data-ttu-id="3452e-147">Exemplo</span><span class="sxs-lookup"><span data-stu-id="3452e-147">Example</span></span>

<span data-ttu-id="3452e-148">Este exemplo usa o método **OpenDatabase** para abrir um banco de dados do Microsoft Access e dois bancos de dados ODBC conectados ao mecanismo de banco de dados do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="3452e-148">This example uses the **OpenDatabase** method to open one Microsoft Access database and two Microsoft Access database engine-connected ODBC databases.</span></span>

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

