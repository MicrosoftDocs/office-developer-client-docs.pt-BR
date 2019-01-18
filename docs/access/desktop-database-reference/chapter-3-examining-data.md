---
title: 'Capítulo 3: Exame de dados'
TOCTitle: 'Chapter 3: Examining data'
ms:assetid: 73c69134-3127-3344-d5c3-5ecb9e0e958b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249474(v=office.15)
ms:contentKeyID: 48545648
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9fcf837a02c40d11fecfa56b8aa34ac80a848411
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28720533"
---
# <a name="chapter-3-examining-data"></a><span data-ttu-id="61a76-102">Capítulo 3: Exame de dados</span><span class="sxs-lookup"><span data-stu-id="61a76-102">Chapter 3: Examining data</span></span>

<span data-ttu-id="61a76-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="61a76-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="61a76-p101">O capítulo 2 explicou como recuperar os dados de uma fonte de dados como um objeto **Recordset**. Este capítulo tratará do **Recordset** mais detalhadamente, incluindo como navegar por meio do **Recordset** e exibir os dados.</span><span class="sxs-lookup"><span data-stu-id="61a76-p101">Chapter 2 explained how to retrieve data from a data source as a **Recordset** object. This chapter will discuss the **Recordset** in more detail, including how to navigate through the **Recordset** and view its data.</span></span>

<span data-ttu-id="61a76-p102">Os **Recordsets** têm métodos e propriedades criados para facilitar o movimento entre eles e examinar os conteúdos deles. Dependendo da funcionalidade oferecida pelo provedor, alguns métodos ou propriedades do **Recordset** poderão não estar disponíveis. Para continuar a exploração do objeto **Recordset**, considere um **Recordset** que será retornado pelo banco de dados de exemplo Northwind no Microsoft SQL Server 2000, usando o seguinte código:</span><span class="sxs-lookup"><span data-stu-id="61a76-p102">**Recordsets** have methods and properties designed to make it easy to move through them and examine their contents. Depending on the functionality supported by the provider, some **Recordset** methods or properties might not be available. To continue exploring the **Recordset** object, consider a **Recordset** that would be returned from the Northwind sample database on Microsoft SQL Server 2000, using the following code:</span></span>

```vb 
 
'BeginRsTour 
Public Sub RecordsetTour() 
 On Error GoTo ErrHandler: 
 
 Dim objRs As New ADODB.Recordset 
 Dim strSQL As String 
 
 strSQL = "SELECT ProductID, ProductName, UnitPrice FROM Products " & _ 
 "WHERE CategoryID = 7" '7 = Produce 
 
 objRs.Open strSQL, strConnStr, adOpenForwardOnly, _ 
 adLockReadOnly, adCmdText 
 
 'Clean up 
 objRs.Close 
 Set objRs = Nothing 
 Exit Sub 
 
ErrHandler: 
 If Not objRs Is Nothing Then 
 If objRs.State = adStateOpen Then objRs.Close 
 Set objRs = Nothing 
 End If 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
'EndRsTour 
```

<br/>

<span data-ttu-id="61a76-p103">Esta consulta SQL retorna um **Recordset** com cinco linhas (registros) e três colunas (campos). Os valores de cada linha são mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="61a76-p103">This SQL query returns a **Recordset** with five rows (records) and three columns (fields). The values for each row are shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="61a76-111">CAMPO 0</span><span class="sxs-lookup"><span data-stu-id="61a76-111">FIELD 0</span></span><br />
<span data-ttu-id="61a76-112">Nome = ProductID</span><span class="sxs-lookup"><span data-stu-id="61a76-112">Name = ProductID</span></span></p></th>
<th><p><span data-ttu-id="61a76-113">CAMPO 1</span><span class="sxs-lookup"><span data-stu-id="61a76-113">FIELD 1</span></span><br />
<span data-ttu-id="61a76-114">Nome = ProductName</span><span class="sxs-lookup"><span data-stu-id="61a76-114">Name = ProductName</span></span></p></th>
<th><p><span data-ttu-id="61a76-115">CAMPO 2</span><span class="sxs-lookup"><span data-stu-id="61a76-115">FIELD 2</span></span><br />
<span data-ttu-id="61a76-116">Nome = UnitPrice</span><span class="sxs-lookup"><span data-stu-id="61a76-116">Name = UnitPrice</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="61a76-117">7</span><span class="sxs-lookup"><span data-stu-id="61a76-117">7</span></span></p></td>
<td><p><span data-ttu-id="61a76-118">Pêras secas orgânicas do Tio Bob</span><span class="sxs-lookup"><span data-stu-id="61a76-118">Uncle Bob's Organic Dried Pears</span></span></p></td>
<td><p><span data-ttu-id="61a76-119">30.0000</span><span class="sxs-lookup"><span data-stu-id="61a76-119">30.0000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61a76-120">14</span><span class="sxs-lookup"><span data-stu-id="61a76-120">14</span></span></p></td>
<td><p><span data-ttu-id="61a76-121">Tofu</span><span class="sxs-lookup"><span data-stu-id="61a76-121">Tofu</span></span></p></td>
<td><p><span data-ttu-id="61a76-122">23.2500</span><span class="sxs-lookup"><span data-stu-id="61a76-122">23.2500</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61a76-123">28</span><span class="sxs-lookup"><span data-stu-id="61a76-123">28</span></span></p></td>
<td><p><span data-ttu-id="61a76-124">Chucrute Rssle</span><span class="sxs-lookup"><span data-stu-id="61a76-124">Rssle Sauerkraut</span></span></p></td>
<td><p><span data-ttu-id="61a76-125">45.6000</span><span class="sxs-lookup"><span data-stu-id="61a76-125">45.6000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61a76-126">51</span><span class="sxs-lookup"><span data-stu-id="61a76-126">51</span></span></p></td>
<td><p><span data-ttu-id="61a76-127">Maçãs secas Manjimup</span><span class="sxs-lookup"><span data-stu-id="61a76-127">Manjimup Dried Apples</span></span></p></td>
<td><p><span data-ttu-id="61a76-128">53.0000</span><span class="sxs-lookup"><span data-stu-id="61a76-128">53.0000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61a76-129">74</span><span class="sxs-lookup"><span data-stu-id="61a76-129">74</span></span></p></td>
<td><p><span data-ttu-id="61a76-130">Tofu longa vida</span><span class="sxs-lookup"><span data-stu-id="61a76-130">Longlife Tofu</span></span></p></td>
<td><p><span data-ttu-id="61a76-131">10.0000</span><span class="sxs-lookup"><span data-stu-id="61a76-131">10.0000</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="61a76-132">A próxima seção explica como localizar a posição atual do cursor neste **Recordset**de exemplo.</span><span class="sxs-lookup"><span data-stu-id="61a76-132">The next section explains how to locate the current position of the cursor in this sample **Recordset**.</span></span>

<span data-ttu-id="61a76-133">Este capítulo aborda os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="61a76-133">This chapter covers the following topics:</span></span>

- [<span data-ttu-id="61a76-134">Localizando o registro atual (ADO)</span><span class="sxs-lookup"><span data-stu-id="61a76-134">Locating the current record (ADO)</span></span>](locating-the-current-record.md)
- [<span data-ttu-id="61a76-135">Navegando nos dados (ADO)</span><span class="sxs-lookup"><span data-stu-id="61a76-135">Navigating through the data (ADO)</span></span>](navigating-through-the-data.md)
- [<span data-ttu-id="61a76-136">Noções básicas sobre a estrutura do Recordset (ADO)</span><span class="sxs-lookup"><span data-stu-id="61a76-136">Understanding Recordset structure (ADO)</span></span>](understanding-recordset-structure.md)
