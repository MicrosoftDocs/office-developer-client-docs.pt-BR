---
title: Método Database.MakeReplica (DAO)
TOCTitle: MakeReplica Method
ms:assetid: b6bf4982-0804-12ce-849f-d2b4ac2e48a5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822413(v=office.15)
ms:contentKeyID: 48547286
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053371
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 9b9e2eac360d157f28b986b6598ade58b8c34ec6
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28711963"
---
# <a name="databasemakereplica-method-dao"></a><span data-ttu-id="cbf42-102">Método Database.MakeReplica (DAO)</span><span class="sxs-lookup"><span data-stu-id="cbf42-102">Database.MakeReplica method (DAO)</span></span>

<span data-ttu-id="cbf42-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="cbf42-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cbf42-104">Cria uma nova réplica a partir de uma outra réplica do banco de dados (somente espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="cbf42-104">Makes a new replica from another database replica (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="cbf42-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cbf42-105">Syntax</span></span>

<span data-ttu-id="cbf42-106">*expressão* . MakeReplica (***PathName***, ***Descrição***, ***Opções***)</span><span class="sxs-lookup"><span data-stu-id="cbf42-106">*expression* .MakeReplica(***PathName***, ***Description***, ***Options***)</span></span>

<span data-ttu-id="cbf42-107">*expressão* Uma variável que representa um objeto de **banco de dados** .</span><span class="sxs-lookup"><span data-stu-id="cbf42-107">*expression* A variable that represents a **Database** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="cbf42-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cbf42-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cbf42-109">Nome</span><span class="sxs-lookup"><span data-stu-id="cbf42-109">Name</span></span></p></th>
<th><p><span data-ttu-id="cbf42-110">Obrigatório/opcional</span><span class="sxs-lookup"><span data-stu-id="cbf42-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="cbf42-111">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="cbf42-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="cbf42-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="cbf42-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cbf42-113"><em>PathName</em></span><span class="sxs-lookup"><span data-stu-id="cbf42-113"><em>PathName</em></span></span></p></td>
<td><p><span data-ttu-id="cbf42-114">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="cbf42-114">Required</span></span></p></td>
<td><p><span data-ttu-id="cbf42-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="cbf42-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="cbf42-p101">O caminho e o nome de arquivo da nova réplica. Se réplica for um nome de arquivo existente, ocorrerá um erro.</span><span class="sxs-lookup"><span data-stu-id="cbf42-p101">The path and file name of the new replica. If replica is an existing file name, then an error occurs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cbf42-118"><em>Descrição</em></span><span class="sxs-lookup"><span data-stu-id="cbf42-118"><em>Description</em></span></span></p></td>
<td><p><span data-ttu-id="cbf42-119">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="cbf42-119">Required</span></span></p></td>
<td><p><span data-ttu-id="cbf42-120"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="cbf42-120"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="cbf42-121">A <strong>String</strong> que descreve a réplica que está sendo criada</span><span class="sxs-lookup"><span data-stu-id="cbf42-121">A <strong>String</strong> that describes the replica that you are creating</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cbf42-122"><em>Options</em></span><span class="sxs-lookup"><span data-stu-id="cbf42-122"><em>Options</em></span></span></p></td>
<td><p><span data-ttu-id="cbf42-123">Opcional</span><span class="sxs-lookup"><span data-stu-id="cbf42-123">Optional</span></span></p></td>
<td><p><span data-ttu-id="cbf42-124"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="cbf42-124"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="cbf42-125">Uma constante <strong><a href="replicatypeenum-enumeration-dao.md">ReplicaTypeEnum</a></strong> que especifica as características da réplica que você está criando.</span><span class="sxs-lookup"><span data-stu-id="cbf42-125">A <strong><a href="replicatypeenum-enumeration-dao.md">ReplicaTypeEnum</a></strong> constant that specifies characteristics of the replica you are creating.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="cbf42-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="cbf42-126">Remarks</span></span>

<span data-ttu-id="cbf42-127">Uma réplica parcial recém-criada terá todas as propriedades **[ReplicaFilter](tabledef-replicafilter-property-dao.md)** definidas como **False**, o que significa que nenhum dado estará nas tabelas.</span><span class="sxs-lookup"><span data-stu-id="cbf42-127">A newly created partial replica will have all **[ReplicaFilter](tabledef-replicafilter-property-dao.md)** properties set to **False**, meaning that no data will be in the tables.</span></span>

## <a name="example"></a><span data-ttu-id="cbf42-128">Exemplo</span><span class="sxs-lookup"><span data-stu-id="cbf42-128">Example</span></span>

<span data-ttu-id="cbf42-129">Esta função usa o método **MakeReplica** para criar uma réplica adicional de um Design Mestre existente.</span><span class="sxs-lookup"><span data-stu-id="cbf42-129">This function uses the **MakeReplica** method to create an additional replica of an existing Design Master.</span></span> <span data-ttu-id="cbf42-130">O argumento intOptions pode ser uma combinação das constantes **dbRepMakeReadOnly** e **dbRepMakePartial**ou pode ser 0.</span><span class="sxs-lookup"><span data-stu-id="cbf42-130">The intOptions argument can be a combination of the constants **dbRepMakeReadOnly** and **dbRepMakePartial**, or it can be 0.</span></span> <span data-ttu-id="cbf42-131">Por exemplo, para criar uma réplica parcial somente leitura, você deve passar o valor **dbRepMakeReadOnly** + **dbRepMakePartial** como o valor do intOptions.</span><span class="sxs-lookup"><span data-stu-id="cbf42-131">For example, to create a read-only partial replica, you should pass the value **dbRepMakeReadOnly** + **dbRepMakePartial** as the value of intOptions.</span></span>

```vb 
Function MakeAdditionalReplica(strReplicableDB As _ 
 String, strNewReplica As String, intOptions As _ 
 Integer) As Integer 
 
 Dim dbsTemp As Database 
 On Error GoTo ErrorHandler 
 
 Set dbsTemp = OpenDatabase(strReplicableDB) 
 
 ' If no options are passed to 
 ' MakeAdditionalReplica, omit the 
 ' options argument, which defaults to 
 ' a full, read/write replica. Otherwise, 
 ' use the value of intOptions. 
 
 If intOptions = 0 Then 
 dbsTemp.MakeReplica strNewReplica, _ 
 "Replica of " & strReplicableDB 
 Else 
 dbsTemp.MakeReplica strNewReplica, _ 
 "Replica of " & strReplicableDB, _ 
 intOptions 
 End If 
 
 dbsTemp.Close 
 
ErrorHandler: 
 Select Case Err 
 Case 0: 
 MakeAdditionalReplica = 0 
 Exit Function 
 Case Else: 
 MsgBox "Error " & Err & " : " & Error 
 MakeAdditionalReplica = Err 
 Exit Function 
 End Select 
 
End Function 
 
```

