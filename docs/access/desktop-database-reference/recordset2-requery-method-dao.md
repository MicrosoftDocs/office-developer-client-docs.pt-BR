---
title: Método Recordset2.Requery (DAO)
TOCTitle: Requery Method
ms:assetid: d063c1e0-2fb7-b5cf-4d98-6f77a5a13cec
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834712(v=office.15)
ms:contentKeyID: 48547837
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052940
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 44f573d179c26677fc801dac82e0deecc3874fb1
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28698537"
---
# <a name="recordset2requery-method-dao"></a><span data-ttu-id="3a13e-102">Método Recordset2.Requery (DAO)</span><span class="sxs-lookup"><span data-stu-id="3a13e-102">Recordset2.Requery method (DAO)</span></span>

<span data-ttu-id="3a13e-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="3a13e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3a13e-104">Atualiza os dados em um objeto **[Recordset](recordset-object-dao.md)** executando novamente a consulta na qual o objeto se baseia.</span><span class="sxs-lookup"><span data-stu-id="3a13e-104">Updates the data in a **[Recordset](recordset-object-dao.md)** object by re-executing the query on which the object is based.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a13e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3a13e-105">Syntax</span></span>

<span data-ttu-id="3a13e-106">*expressão* . Requery (***novadefiniçãodaconsulta***)</span><span class="sxs-lookup"><span data-stu-id="3a13e-106">*expression* .Requery(***NewQueryDef***)</span></span>

<span data-ttu-id="3a13e-107">*expressão* Uma variável que representa um objeto **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="3a13e-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="3a13e-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3a13e-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3a13e-109">Nome</span><span class="sxs-lookup"><span data-stu-id="3a13e-109">Name</span></span></p></th>
<th><p><span data-ttu-id="3a13e-110">Obrigatório/opcional</span><span class="sxs-lookup"><span data-stu-id="3a13e-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="3a13e-111">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="3a13e-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="3a13e-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="3a13e-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3a13e-113"><em>Novadefiniçãodaconsulta</em></span><span class="sxs-lookup"><span data-stu-id="3a13e-113"><em>NewQueryDef</em></span></span></p></td>
<td><p><span data-ttu-id="3a13e-114">Opcional</span><span class="sxs-lookup"><span data-stu-id="3a13e-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="3a13e-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="3a13e-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="3a13e-116">Representa o valor da propriedade <strong>Name</strong> de um objeto <strong><a href="querydef-object-dao.md">QueryDef</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="3a13e-116">Represents the <strong>Name</strong> property value of a <strong><a href="querydef-object-dao.md">QueryDef</a></strong> object</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="3a13e-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="3a13e-117">Remarks</span></span>

<span data-ttu-id="3a13e-118">Use esse método para verificar se um **Recordset** contém os dados mais recentes.</span><span class="sxs-lookup"><span data-stu-id="3a13e-118">Use this method to make sure that a **Recordset** contains the most recent data.</span></span> <span data-ttu-id="3a13e-119">Esse método preenche novamente o **Recordset** atual usando os parâmetros consulta atual ou (em um espaço de trabalho do Microsoft Access) os novos parâmetros fornecidos pelo argumento novadefiniçãodaconsulta.</span><span class="sxs-lookup"><span data-stu-id="3a13e-119">This method re-populates the current **Recordset** by using either the current query parameters or (in a Microsoft Access workspace) the new ones supplied by the newquerydef argument.</span></span>

<span data-ttu-id="3a13e-120">Se você não especificar um argumento novadefiniçãodaconsulta, o **Recordset** será preenchido novamente com base na mesma definição de consulta e os parâmetros usados para preencher originalmente o **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="3a13e-120">If you don't specify a newquerydef argument, the **Recordset** is re-populated based on the same query definition and parameters used to originally populate the **Recordset**.</span></span> <span data-ttu-id="3a13e-121">Qualquer alteração nos dados de base será refletida durante esse repreenchimento.</span><span class="sxs-lookup"><span data-stu-id="3a13e-121">Any changes to the underlying data will be reflected during this re-population.</span></span> <span data-ttu-id="3a13e-122">Se você não usou **QueryDef** para criar o **Recordset**, o **Recordset** é recriado do zero.</span><span class="sxs-lookup"><span data-stu-id="3a13e-122">If you didn't use a **QueryDef** to create the **Recordset**, the **Recordset** is re-created from scratch.</span></span>

<span data-ttu-id="3a13e-123">Se você especificar um **QueryDef** original no argumento novadefiniçãodaconsulta, em seguida, o **Recordset** é consultado novamente usando os parâmetros especificados por **QueryDef**.</span><span class="sxs-lookup"><span data-stu-id="3a13e-123">If you specify the original **QueryDef** in the newquerydef argument, then the **Recordset** is requeried using the parameters specified by the **QueryDef**.</span></span> <span data-ttu-id="3a13e-124">Qualquer alteração nos dados de base será refletida durante esse repreenchimento.</span><span class="sxs-lookup"><span data-stu-id="3a13e-124">Any changes to the underlying data will be reflected during this re-population.</span></span> <span data-ttu-id="3a13e-125">Para refletir as alterações para os valores de parâmetro de consulta no **Recordset**, você deve fornecer o argumento novadefiniçãodaconsulta.</span><span class="sxs-lookup"><span data-stu-id="3a13e-125">To reflect any changes to the query parameter values in the **Recordset**, you must supply the newquerydef argument.</span></span>

<span data-ttu-id="3a13e-126">Se você especificar um **QueryDef** diferente do originalmente utilizado para criar o **Recordset**, o **Recordset** será recriado do zero.</span><span class="sxs-lookup"><span data-stu-id="3a13e-126">If you specify a different **QueryDef** than what was originally used to create the **Recordset**, the **Recordset** is re-created from scratch.</span></span>

<span data-ttu-id="3a13e-127">Quando você usa **Requery**, o primeiro registro no **Recordset** torna-se o registro atual.</span><span class="sxs-lookup"><span data-stu-id="3a13e-127">When you use **Requery**, the first record in the **Recordset** becomes the current record.</span></span>

<span data-ttu-id="3a13e-128">Você não pode usar o método **Requery** nos objetos **Recordset** do tipo dynaset ou instantâneo cuja propriedade **[Restartable](recordset2-restartable-property-dao.md)** está definida como **False**.</span><span class="sxs-lookup"><span data-stu-id="3a13e-128">You can't use the **Requery** method on dynaset- or snapshot-type **Recordset** objects whose **[Restartable](recordset2-restartable-property-dao.md)** property is set to **False**.</span></span> <span data-ttu-id="3a13e-129">No entanto, se você fornecer o argumento opcional novadefiniçãodaconsulta, a propriedade **Restartable** será ignorada.</span><span class="sxs-lookup"><span data-stu-id="3a13e-129">However, if you supply the optional newquerydef argument, the **Restartable** property is ignored.</span></span>

<span data-ttu-id="3a13e-130">Se as configurações das propriedades **[BOF](recordset2-bof-property-dao.md)** e **[EOF](recordset2-eof-property-dao.md)** do objeto **Recordset** forem **True** após a utilização do método **Requery**, a consulta não retornará nenhum registro, e o **Recordset** não conterá nenhum dado.</span><span class="sxs-lookup"><span data-stu-id="3a13e-130">If both the **[BOF](recordset2-bof-property-dao.md)** and **[EOF](recordset2-eof-property-dao.md)** property settings of the **Recordset** object are **True** after you use the **Requery** method, the query didn't return any records and the **Recordset** contains no data.</span></span>

## <a name="example"></a><span data-ttu-id="3a13e-131">Exemplo</span><span class="sxs-lookup"><span data-stu-id="3a13e-131">Example</span></span>

<span data-ttu-id="3a13e-132">Este exemplo mostra como o método **Requery** pode ser utilizado para atualizar uma consulta após a alteração dos dados de base.</span><span class="sxs-lookup"><span data-stu-id="3a13e-132">This example shows how the **Requery** method can be used to refresh a query after underlying data has been changed.</span></span>

```vb
    Sub RequeryX() 
     
     Dim dbsNorthwind As Database 
     Dim qdfTemp As QueryDef 
     Dim rstView As Recordset2 
     Dim rstChange As Recordset2 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set qdfTemp = dbsNorthwind.CreateQueryDef("", _ 
     "PARAMETERS ViewCountry Text; " & _ 
     "SELECT FirstName, LastName, Country FROM " & _ 
     "Employees WHERE Country = [ViewCountry] " & _ 
     "ORDER BY LastName") 
     
     qdfTemp.Parameters!ViewCountry = "USA" 
     Debug.Print "Data after initial query, " & _ 
     [ViewCountry] = USA" 
     Set rstView = qdfTemp.OpenRecordset 
     Do While Not rstView.EOF 
     Debug.Print " " & rstView!FirstName & " " & _ 
     rstView!LastName & ", " & rstView!Country 
     rstView.MoveNext 
     Loop 
     
     ' Change underlying data. 
     Set rstChange = dbsNorthwind.OpenRecordset("Employees") 
     rstChange.AddNew 
     rstChange!FirstName = "Nina" 
     rstChange!LastName = "Roberts" 
     rstChange!Country = "USA" 
     rstChange.Update 
     
     rstView.Requery 
     Debug.Print "Requery after changing underlying data" 
     Set rstView = qdfTemp.OpenRecordset 
     Do While Not rstView.EOF 
     Debug.Print " " & rstView!FirstName & " " & _ 
     rstView!LastName & ", " & rstView!Country 
     rstView.MoveNext 
     Loop 
     
     ' Restore original data because this is only a 
     ' demonstration. 
     rstChange.Bookmark = rstChange.LastModified 
     rstChange.Delete 
     rstChange.Close 
     
     rstView.Close 
     dbsNorthwind.Close 
     
    End Sub 
```

<br/>

<span data-ttu-id="3a13e-133">Este exemplo mostra como o método **Requery** pode ser utilizado para atualizar uma consulta após a alteração dos parâmetros de consulta.</span><span class="sxs-lookup"><span data-stu-id="3a13e-133">This example shows how the **Requery** method can be used to refresh a query after the query parameters have been changed.</span></span>

```vb
Sub RequeryX2() 
 
 Dim dbsNorthwind As Database 
 Dim qdfTemp As QueryDef 
 Dim prmCountry As Parameter 
 Dim rstView As Recordset2 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 Set qdfTemp = dbsNorthwind.CreateQueryDef("", _ 
 "PARAMETERS ViewCountry Text; " & _ 
 "SELECT FirstName, LastName, Country FROM " & _ 
 "Employees WHERE Country = [ViewCountry] " & _ 
 "ORDER BY LastName") 
 Set prmCountry = qdfTemp.Parameters!ViewCountry 
 
 qdfTemp.Parameters!ViewCountry = "USA" 
 Debug.Print "Data after initial query, " & _ 
 [ViewCountry] = USA" 
 Set rstView = qdfTemp.OpenRecordset 
 Do While Not rstView.EOF 
 Debug.Print " " & rstView!FirstName & " " & _ 
 rstView!LastName & ", " & rstView!Country 
 rstView.MoveNext 
 Loop 
 
 ' Change query parameter. 
 qdfTemp.Parameters!ViewCountry = "UK" 
 ' QueryDef argument must be included so that the 
 ' resulting Recordset reflects the change in the query 
 ' parameter. 
 rstView.Requery qdfTemp 
 Debug.Print "Requery after changing parameter, " & _ 
 "[ViewCountry] = UK" 
 Do While Not rstView.EOF 
 Debug.Print " " & rstView!FirstName & " " & _ 
 rstView!LastName & ", " & rstView!Country 
 rstView.MoveNext 
 Loop 
 
 rstView.Close 
 dbsNorthwind.Close 
 
End Sub 
 
```

