---
title: Método DBEngine.RegisterDatabase (DAO)
TOCTitle: RegisterDatabase Method
ms:assetid: ed87a694-2c89-0a78-5d8b-0cc7e09fadff
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836347(v=office.15)
ms:contentKeyID: 48548541
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052938
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 304f517d11e6e333bb0455e3882421c410c56b72
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462946"
---
# <a name="dbengineregisterdatabase-method-dao"></a><span data-ttu-id="d614b-102">Método DBEngine.RegisterDatabase (DAO)</span><span class="sxs-lookup"><span data-stu-id="d614b-102">DBEngine.RegisterDatabase Method (DAO)</span></span>


<span data-ttu-id="d614b-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="d614b-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="d614b-p101">Insere as informações de conexão para uma fonte de dados ODBC no Registro do Windows. O driver ODBC precisa das informações de conexão quando a fonte de dados ODBC é aberta durante uma sessão.</span><span class="sxs-lookup"><span data-stu-id="d614b-p101">Enters connection information for an ODBC data source in the Windows Registry. The ODBC driver needs connection information when the ODBC data source is opened during a session.</span></span>

## <a name="syntax"></a><span data-ttu-id="d614b-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d614b-106">Syntax</span></span>

<span data-ttu-id="d614b-107">*expressão* . RegisterDatabase (***Dsn***, ***Driver***, ***silenciosa***, ***atributos***)</span><span class="sxs-lookup"><span data-stu-id="d614b-107">*expression* .RegisterDatabase(***Dsn***, ***Driver***, ***Silent***, ***Attributes***)</span></span>

<span data-ttu-id="d614b-108">*expressão* Uma variável que representa um objeto **DBEngine** .</span><span class="sxs-lookup"><span data-stu-id="d614b-108">*expression* A variable that represents a **DBEngine** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="d614b-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d614b-109">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d614b-110">Nome</span><span class="sxs-lookup"><span data-stu-id="d614b-110">Name</span></span></p></th>
<th><p><span data-ttu-id="d614b-111">Obrigatório/Opcional</span><span class="sxs-lookup"><span data-stu-id="d614b-111">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="d614b-112">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="d614b-112">Data Type</span></span></p></th>
<th><p><span data-ttu-id="d614b-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="d614b-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d614b-114">DSN</span><span class="sxs-lookup"><span data-stu-id="d614b-114">Dsn</span></span></p></td>
<td><p><span data-ttu-id="d614b-115">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="d614b-115">Required</span></span></p></td>
<td><p><span data-ttu-id="d614b-116"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="d614b-116"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="d614b-p102">O nome usado no método <strong><a href="dbengine-opendatabase-method-dao.md">OpenDatabase</a></strong>. Ele se refere a um bloco de informações descritivas sobre a fonte de dados. Por exemplo, se a fonte de dados for um banco de dados remoto ODBC, ele poderá ser o nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="d614b-p102">the name used in the <strong><a href="dbengine-opendatabase-method-dao.md">OpenDatabase</a></strong> method. It refers to a block of descriptive information about the data source. For example, if the data source is an ODBC remote database, it could be the name of the server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d614b-120">Driver</span><span class="sxs-lookup"><span data-stu-id="d614b-120">Driver</span></span></p></td>
<td><p><span data-ttu-id="d614b-121">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="d614b-121">Required</span></span></p></td>
<td><p><span data-ttu-id="d614b-122"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="d614b-122"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="d614b-p103">O nome do driver ODBC. Esse não é o nome do arquivo DLL do driver ODBC.</span><span class="sxs-lookup"><span data-stu-id="d614b-p103">The name of the ODBC driver. This isn't the name of the ODBC driver DLL file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d614b-125">Silenciosa</span><span class="sxs-lookup"><span data-stu-id="d614b-125">Silent</span></span></p></td>
<td><p><span data-ttu-id="d614b-126">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="d614b-126">Required</span></span></p></td>
<td><p><span data-ttu-id="d614b-127"><strong>Boolean</strong></span><span class="sxs-lookup"><span data-stu-id="d614b-127"><strong>Boolean</strong></span></span></p></td>
<td><p><span data-ttu-id="d614b-128"><strong>True</strong> se você não quiser exibir as caixas de diálogo de driver ODBC que solicita informações específicas do driver; ou <strong>False</strong> se você deseja exibir as caixas de diálogo do driver ODBC.</span><span class="sxs-lookup"><span data-stu-id="d614b-128"><strong>True</strong> if you don't want to display the ODBC driver dialog boxes that prompt for driver-specific information; or <strong>False</strong> if you want to display the ODBC driver dialog boxes.</span></span> <span data-ttu-id="d614b-129">Se silenciosa for <strong>True</strong>, atributos devem conter todas as informações necessárias específicas do driver ou as caixas de diálogo serão exibidas mesmo assim.</span><span class="sxs-lookup"><span data-stu-id="d614b-129">If silent is <strong>True</strong>, attributes must contain all the necessary driver-specific information or the dialog boxes are displayed anyway.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d614b-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="d614b-130">Attributes</span></span></p></td>
<td><p><span data-ttu-id="d614b-131">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="d614b-131">Required</span></span></p></td>
<td><p><span data-ttu-id="d614b-132"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="d614b-132"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="d614b-p105">Uma lista de palavras-chave a serem adicionadas ao Registro do Windows. As palavras-chave estão em uma sequência delimitada por retorno de carro.</span><span class="sxs-lookup"><span data-stu-id="d614b-p105">A list of keywords to be added to the Windows Registry. The keywords are in a carriage-return–delimited string.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="d614b-135">Comentários</span><span class="sxs-lookup"><span data-stu-id="d614b-135">Remarks</span></span>

<span data-ttu-id="d614b-136">Se o banco de dados já estiver registrado (as informações de conexão já estarão inseridas) no Registro do Windows quando você usar o método **RegisterDatabase**, as informações de conexão serão atualizadas.</span><span class="sxs-lookup"><span data-stu-id="d614b-136">If the database is already registered (connection information is already entered) in the Windows Registry when you use the **RegisterDatabase** method, the connection information is updated.</span></span>

<span data-ttu-id="d614b-137">Se o método **RegisterDatabase** falhar por qualquer motivo, nenhuma alteração será feita no Registro do Windows, e ocorrerá um erro.</span><span class="sxs-lookup"><span data-stu-id="d614b-137">If the **RegisterDatabase** method fails for any reason, no changes are made to the Windows Registry, and an error occurs.</span></span>

<span data-ttu-id="d614b-138">Para obter mais informações sobre drivers ODBC, como SQL Server, consulte o arquivo de Ajuda fornecido com o driver.</span><span class="sxs-lookup"><span data-stu-id="d614b-138">For more information about ODBC drivers such as SQL Server, see the Help file provided with the driver.</span></span>

## <a name="example"></a><span data-ttu-id="d614b-139">Exemplo</span><span class="sxs-lookup"><span data-stu-id="d614b-139">Example</span></span>

<span data-ttu-id="d614b-140">Este exemplo utiliza o método **RegisterDatabase** para registrar uma fonte de dados do Microsoft SQL Server chamada Publishers no Registro do Windows.</span><span class="sxs-lookup"><span data-stu-id="d614b-140">This example uses the **RegisterDatabase** method to register a Microsoft SQL Server data source named Publishers in the Windows Registry.</span></span>

```vb 
Sub RegisterDatabaseX() 
 
 Dim dbsRegister As Database 
 Dim strDescription As String 
 Dim strAttributes As String 
 Dim errLoop As Error 
 
 ' Build keywords string. 
 strDescription = InputBox( "Enter a description " & _ 
 "for the database to be registered.") 
 strAttributes = "Database=pubs" & _ 
 vbCr & "Description=" & strDescription & _ 
 vbCr & "OemToAnsi=No" & _ 
 vbCr & "Server=Server1" 
 
 ' Update Windows Registry. 
 On Error GoTo Err_Register 
 DBEngine.RegisterDatabase "Publishers", "SQL Server", _ 
 True, strAttributes 
 On Error GoTo 0 
 
 MsgBox "Use regedit.exe to view changes: " & _ 
 "HKEY_CURRENT_USER\" & _ 
 "Software\ODBC\ODBC.INI" 
 
 Exit Sub 
 
Err_Register: 
 
 ' Notify user of any errors that result from 
 ' the invalid data. 
 If DBEngine.Errors.Count > 0 Then 
 For Each errLoop In DBEngine.Errors 
 MsgBox "Error number: " & errLoop.Number & _ 
 vbCr & errLoop.Description 
 Next errLoop 
 End If 
 
 Resume Next 
 
End Sub 
 
```

