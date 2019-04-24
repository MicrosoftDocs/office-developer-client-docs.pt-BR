---
title: Método DBEngine. setOption (DAO)
TOCTitle: SetOption Method
ms:assetid: ea55c10c-2385-1b7e-0cba-32982c9b6643
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836236(v=office.15)
ms:contentKeyID: 48548461
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1088781
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 5875a8935b1b44c3c36b29344af32df552f6e01c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294194"
---
# <a name="dbenginesetoption-method-dao"></a><span data-ttu-id="77e31-102">Método DBEngine. setOption (DAO)</span><span class="sxs-lookup"><span data-stu-id="77e31-102">DBEngine.SetOption method (DAO)</span></span>

<span data-ttu-id="77e31-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="77e31-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="77e31-104">Substitui temporariamente os valores para as chaves do mecanismo de banco de dados do Microsoft Access no Registro do Windows (somente espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="77e31-104">Temporarily overrides values for the Microsoft Access database engine keys in the Windows Registry (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="77e31-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="77e31-105">Syntax</span></span>

<span data-ttu-id="77e31-106">*expressão* . SetOption (***opção***, ***valor***)</span><span class="sxs-lookup"><span data-stu-id="77e31-106">*expression* .SetOption(***Option***, ***Value***)</span></span>

<span data-ttu-id="77e31-107">*expressão* Uma expressão que retorna um objeto **DBEngine** .</span><span class="sxs-lookup"><span data-stu-id="77e31-107">*expression* An expression that returns a **DBEngine** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="77e31-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="77e31-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="77e31-109">Nome</span><span class="sxs-lookup"><span data-stu-id="77e31-109">Name</span></span></p></th>
<th><p><span data-ttu-id="77e31-110">Obrigatório/opcional</span><span class="sxs-lookup"><span data-stu-id="77e31-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="77e31-111">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="77e31-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="77e31-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="77e31-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="77e31-113"><em>Opção</em></span><span class="sxs-lookup"><span data-stu-id="77e31-113"><em>Option</em></span></span></p></td>
<td><p><span data-ttu-id="77e31-114">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="77e31-114">Required</span></span></p></td>
<td><p><span data-ttu-id="77e31-115"><strong>Long</strong></span><span class="sxs-lookup"><span data-stu-id="77e31-115"><strong>Long</strong></span></span></p></td>
<td><p><span data-ttu-id="77e31-116">Uma constante como descrita em Comentários.</span><span class="sxs-lookup"><span data-stu-id="77e31-116">A constant as described in Remarks.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77e31-117"><em>Value</em></span><span class="sxs-lookup"><span data-stu-id="77e31-117"><em>Value</em></span></span></p></td>
<td><p><span data-ttu-id="77e31-118">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="77e31-118">Required</span></span></p></td>
<td><p><span data-ttu-id="77e31-119"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="77e31-119"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="77e31-120">O valor para o qual você deseja definir a opção.</span><span class="sxs-lookup"><span data-stu-id="77e31-120">The value that you want to set option to.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="77e31-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="77e31-121">Remarks</span></span>

<span data-ttu-id="77e31-122">Cada constante se refere à chave do registro correspondente no caminho HKEY\_local\_MACHINE\\software\\Microsoft\\Office\\12,0\\Access Connectivity\\Engines\\, ACE (ou seja, **dbSharedAsyncDelay** corresponde à chave hKey\_local\_Machine\\software\\Microsoft\\Office\\12,0\\Access Connectivity Engines\\\\Ace \\SharedAsyncDelay e assim por diante).</span><span class="sxs-lookup"><span data-stu-id="77e31-122">Each constant refers to the corresponding registry key in the path HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Office\\12.0\\Access Connectivity Engine\\Engines\\ACE (that is, **dbSharedAsyncDelay** corresponds to the key HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Office\\12.0\\Access Connectivity Engine\\Engines\\ACE\\SharedAsyncDelay, and so on).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="77e31-123">Constante</span><span class="sxs-lookup"><span data-stu-id="77e31-123">Constant</span></span></p></th>
<th><p><span data-ttu-id="77e31-124">Descrição</span><span class="sxs-lookup"><span data-stu-id="77e31-124">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="77e31-125"><strong>dbPageTimeout</strong></span><span class="sxs-lookup"><span data-stu-id="77e31-125"><strong>dbPageTimeout</strong></span></span></p></td>
<td><p><span data-ttu-id="77e31-126">A chave PageTimeout</span><span class="sxs-lookup"><span data-stu-id="77e31-126">The PageTimeout key</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77e31-127"><strong>dbSharedAsyncDelay</strong></span><span class="sxs-lookup"><span data-stu-id="77e31-127"><strong>dbSharedAsyncDelay</strong></span></span></p></td>
<td><p><span data-ttu-id="77e31-128">A chave SharedAsyncDelay</span><span class="sxs-lookup"><span data-stu-id="77e31-128">The SharedAsyncDelay key</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77e31-129"><strong>dbExclusiveAsyncDelay</strong></span><span class="sxs-lookup"><span data-stu-id="77e31-129"><strong>dbExclusiveAsyncDelay</strong></span></span></p></td>
<td><p><span data-ttu-id="77e31-130">A chave ExclusiveAsyncDelay</span><span class="sxs-lookup"><span data-stu-id="77e31-130">The ExclusiveAsyncDelay key</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77e31-131"><strong>dbLockRetry</strong></span><span class="sxs-lookup"><span data-stu-id="77e31-131"><strong>dbLockRetry</strong></span></span></p></td>
<td><p><span data-ttu-id="77e31-132">A chave LockRetry</span><span class="sxs-lookup"><span data-stu-id="77e31-132">The LockRetry key</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77e31-133"><strong>dbUserCommitSync</strong></span><span class="sxs-lookup"><span data-stu-id="77e31-133"><strong>dbUserCommitSync</strong></span></span></p></td>
<td><p><span data-ttu-id="77e31-134">A chave UserCommitSync</span><span class="sxs-lookup"><span data-stu-id="77e31-134">The UserCommitSync key</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77e31-135"><strong>dbImplicitCommitSync</strong></span><span class="sxs-lookup"><span data-stu-id="77e31-135"><strong>dbImplicitCommitSync</strong></span></span></p></td>
<td><p><span data-ttu-id="77e31-136">A chave ImplicitCommitSync</span><span class="sxs-lookup"><span data-stu-id="77e31-136">The ImplicitCommitSync key</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77e31-137"><strong>dbMaxBufferSize</strong></span><span class="sxs-lookup"><span data-stu-id="77e31-137"><strong>dbMaxBufferSize</strong></span></span></p></td>
<td><p><span data-ttu-id="77e31-138">A chave MaxBufferSize</span><span class="sxs-lookup"><span data-stu-id="77e31-138">The MaxBufferSize key</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77e31-139"><strong>dbMaxLocksPerFile</strong></span><span class="sxs-lookup"><span data-stu-id="77e31-139"><strong>dbMaxLocksPerFile</strong></span></span></p></td>
<td><p><span data-ttu-id="77e31-140">A chave MaxLocksPerFile</span><span class="sxs-lookup"><span data-stu-id="77e31-140">The MaxLocksPerFile key</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77e31-141"><strong>dbLockDelay</strong></span><span class="sxs-lookup"><span data-stu-id="77e31-141"><strong>dbLockDelay</strong></span></span></p></td>
<td><p><span data-ttu-id="77e31-142">A chave LockDelay</span><span class="sxs-lookup"><span data-stu-id="77e31-142">The LockDelay key</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77e31-143"><strong>dbRecycleLVs</strong></span><span class="sxs-lookup"><span data-stu-id="77e31-143"><strong>dbRecycleLVs</strong></span></span></p></td>
<td><p><span data-ttu-id="77e31-144">A chave RecycleLVs</span><span class="sxs-lookup"><span data-stu-id="77e31-144">The RecycleLVs key</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77e31-145"><strong>dbFlushTransactionTimeout</strong></span><span class="sxs-lookup"><span data-stu-id="77e31-145"><strong>dbFlushTransactionTimeout</strong></span></span></p></td>
<td><p><span data-ttu-id="77e31-146">A chave FlushTransactionTimeout</span><span class="sxs-lookup"><span data-stu-id="77e31-146">The FlushTransactionTimeout key</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="77e31-p101">Use o método **SetOption** para substituir os valores do Registro no tempo de execução. Novos valores estabelecidos com o método **SetOption** permanecem vigentes até que sejam alterados novamente por outra chamada **SetOption** ou até que o objeto **DBEngine** seja fechado.</span><span class="sxs-lookup"><span data-stu-id="77e31-p101">Use the **SetOption** method to override registry values at run-time. New values established with the **SetOption** method remain in effect until changed again by another **SetOption** call, or until the **DBEngine** object is closed.</span></span>

