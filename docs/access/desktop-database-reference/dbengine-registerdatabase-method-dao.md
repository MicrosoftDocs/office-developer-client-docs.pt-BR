---
title: Método DBEngine. RegisterDatabase (DAO)
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
localization_priority: Normal
ms.openlocfilehash: 632f6e10d79d74dfef295b34a52ce62f1690101b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294222"
---
# <a name="dbengineregisterdatabase-method-dao"></a><span data-ttu-id="dc987-102">Método DBEngine. RegisterDatabase (DAO)</span><span class="sxs-lookup"><span data-stu-id="dc987-102">DBEngine.RegisterDatabase method (DAO)</span></span>

<span data-ttu-id="dc987-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="dc987-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="dc987-p101">Insere as informações de conexão para uma fonte de dados ODBC no Registro do Windows. O driver ODBC precisa das informações de conexão quando a fonte de dados ODBC é aberta durante uma sessão.</span><span class="sxs-lookup"><span data-stu-id="dc987-p101">Enters connection information for an ODBC data source in the Windows Registry. The ODBC driver needs connection information when the ODBC data source is opened during a session.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc987-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dc987-106">Syntax</span></span>

<span data-ttu-id="dc987-107">*expressão* . RegisterDatabase (***DSN***, ***Driver***, ***silencioso***, ***atributos***)</span><span class="sxs-lookup"><span data-stu-id="dc987-107">*expression* .RegisterDatabase(***Dsn***, ***Driver***, ***Silent***, ***Attributes***)</span></span>

<span data-ttu-id="dc987-108">*expressão* Uma variável que representa um objeto **DBEngine** .</span><span class="sxs-lookup"><span data-stu-id="dc987-108">*expression* A variable that represents a **DBEngine** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="dc987-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dc987-109">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="dc987-110">Nome</span><span class="sxs-lookup"><span data-stu-id="dc987-110">Name</span></span></p></th>
<th><p><span data-ttu-id="dc987-111">Obrigatório/opcional</span><span class="sxs-lookup"><span data-stu-id="dc987-111">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="dc987-112">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="dc987-112">Data type</span></span></p></th>
<th><p><span data-ttu-id="dc987-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="dc987-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dc987-114"><em>DSN</em></span><span class="sxs-lookup"><span data-stu-id="dc987-114"><em>Dsn</em></span></span></p></td>
<td><p><span data-ttu-id="dc987-115">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="dc987-115">Required</span></span></p></td>
<td><p><span data-ttu-id="dc987-116"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="dc987-116"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="dc987-117">o nome usado no método <strong><a href="dbengine-opendatabase-method-dao.md">OpenDatabase</a></strong> .</span><span class="sxs-lookup"><span data-stu-id="dc987-117">the name used in the <strong><a href="dbengine-opendatabase-method-dao.md">OpenDatabase</a></strong> method.</span></span> <span data-ttu-id="dc987-118">Ele se refere a um bloco de informações descritivas sobre a fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="dc987-118">It refers to a block of descriptive information about the data source.</span></span> <span data-ttu-id="dc987-119">Por exemplo, se a fonte de dados for um banco de dados remoto ODBC, ele poderá ser o nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="dc987-119">For example, if the data source is an ODBC remote database, it could be the name of the server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc987-120"><em>Driver</em></span><span class="sxs-lookup"><span data-stu-id="dc987-120"><em>Driver</em></span></span></p></td>
<td><p><span data-ttu-id="dc987-121">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="dc987-121">Required</span></span></p></td>
<td><p><span data-ttu-id="dc987-122"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="dc987-122"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="dc987-123">O nome do driver ODBC.</span><span class="sxs-lookup"><span data-stu-id="dc987-123">The name of the ODBC driver.</span></span> <span data-ttu-id="dc987-124">Esse não é o nome do arquivo DLL do driver ODBC.</span><span class="sxs-lookup"><span data-stu-id="dc987-124">This isn't the name of the ODBC driver DLL file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc987-125"><em>Silenciosa</em></span><span class="sxs-lookup"><span data-stu-id="dc987-125"><em>Silent</em></span></span></p></td>
<td><p><span data-ttu-id="dc987-126">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="dc987-126">Required</span></span></p></td>
<td><p><span data-ttu-id="dc987-127"><strong>Boolean</strong></span><span class="sxs-lookup"><span data-stu-id="dc987-127"><strong>Boolean</strong></span></span></p></td>
<td><p><span data-ttu-id="dc987-128"><strong>True</strong> se você não quiser exibir as caixas de diálogo do driver ODBC que solicitam as informações específicas do driver; ou <strong>False</strong> se você desejar exibir as caixas de diálogo do driver ODBC.</span><span class="sxs-lookup"><span data-stu-id="dc987-128"><strong>True</strong> if you don't want to display the ODBC driver dialog boxes that prompt for driver-specific information; or <strong>False</strong> if you want to display the ODBC driver dialog boxes.</span></span> <span data-ttu-id="dc987-129">Se silencioso for <strong>verdadeiro</strong>, os atributos deverão conter todas as informações específicas do driver necessárias ou as caixas de diálogo serão exibidas de qualquer forma.</span><span class="sxs-lookup"><span data-stu-id="dc987-129">If silent is <strong>True</strong>, attributes must contain all the necessary driver-specific information or the dialog boxes are displayed anyway.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc987-130"><em>Atributos</em></span><span class="sxs-lookup"><span data-stu-id="dc987-130"><em>Attributes</em></span></span></p></td>
<td><p><span data-ttu-id="dc987-131">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="dc987-131">Required</span></span></p></td>
<td><p><span data-ttu-id="dc987-132"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="dc987-132"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="dc987-133">Uma lista de palavras-chave a serem adicionadas ao Registro do Windows.</span><span class="sxs-lookup"><span data-stu-id="dc987-133">A list of keywords to be added to the Windows Registry.</span></span> <span data-ttu-id="dc987-134">As palavras-chave estão em uma sequência delimitada por retorno de carro.</span><span class="sxs-lookup"><span data-stu-id="dc987-134">The keywords are in a carriage-return–delimited string.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="dc987-135">Comentários</span><span class="sxs-lookup"><span data-stu-id="dc987-135">Remarks</span></span>

<span data-ttu-id="dc987-136">Se o banco de dados já estiver registrado (as informações de conexão já estarão inseridas) no Registro do Windows quando você usar o método **RegisterDatabase**, as informações de conexão serão atualizadas.</span><span class="sxs-lookup"><span data-stu-id="dc987-136">If the database is already registered (connection information is already entered) in the Windows Registry when you use the **RegisterDatabase** method, the connection information is updated.</span></span>

<span data-ttu-id="dc987-137">Se o método **RegisterDatabase** falhar por qualquer motivo, nenhuma alteração será feita no Registro do Windows, e ocorrerá um erro.</span><span class="sxs-lookup"><span data-stu-id="dc987-137">If the **RegisterDatabase** method fails for any reason, no changes are made to the Windows Registry, and an error occurs.</span></span>

<span data-ttu-id="dc987-138">Para obter mais informações sobre drivers ODBC, como SQL Server, consulte o arquivo de Ajuda fornecido com o driver.</span><span class="sxs-lookup"><span data-stu-id="dc987-138">For more information about ODBC drivers such as SQL Server, see the Help file provided with the driver.</span></span>

## <a name="example"></a><span data-ttu-id="dc987-139">Exemplo</span><span class="sxs-lookup"><span data-stu-id="dc987-139">Example</span></span>

<span data-ttu-id="dc987-140">Este exemplo utiliza o método **RegisterDatabase** para registrar uma fonte de dados do Microsoft SQL Server chamada Publishers no Registro do Windows.</span><span class="sxs-lookup"><span data-stu-id="dc987-140">This example uses the **RegisterDatabase** method to register a Microsoft SQL Server data source named Publishers in the Windows Registry.</span></span>

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

