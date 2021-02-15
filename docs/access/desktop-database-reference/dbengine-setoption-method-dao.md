---
title: Método DBEngine.SetOption (DAO)
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
# <a name="dbenginesetoption-method-dao"></a><span data-ttu-id="73bf8-102">Método DBEngine.SetOption (DAO)</span><span class="sxs-lookup"><span data-stu-id="73bf8-102">DBEngine.SetOption method (DAO)</span></span>

<span data-ttu-id="73bf8-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="73bf8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="73bf8-104">Substitui temporariamente os valores para as chaves do mecanismo de banco de dados do Microsoft Access no Registro do Windows (somente espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="73bf8-104">Temporarily overrides values for the Microsoft Access database engine keys in the Windows Registry (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="73bf8-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="73bf8-105">Syntax</span></span>

<span data-ttu-id="73bf8-106">*expressão* . SetOption(***Option***, ***Value***)</span><span class="sxs-lookup"><span data-stu-id="73bf8-106">*expression* .SetOption(***Option***, ***Value***)</span></span>

<span data-ttu-id="73bf8-107">*expressão* Uma expressão que retorna um objeto **DBEngine**.</span><span class="sxs-lookup"><span data-stu-id="73bf8-107">*expression* An expression that returns a **DBEngine** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="73bf8-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="73bf8-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="73bf8-109">Nome</span><span class="sxs-lookup"><span data-stu-id="73bf8-109">Name</span></span></p></th>
<th><p><span data-ttu-id="73bf8-110">Necessária/opcional</span><span class="sxs-lookup"><span data-stu-id="73bf8-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="73bf8-111">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="73bf8-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="73bf8-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="73bf8-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="73bf8-113"><em>Opção</em></span><span class="sxs-lookup"><span data-stu-id="73bf8-113"><em>Option</em></span></span></p></td>
<td><p><span data-ttu-id="73bf8-114">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="73bf8-114">Required</span></span></p></td>
<td><p><span data-ttu-id="73bf8-115"><strong>Long</strong></span><span class="sxs-lookup"><span data-stu-id="73bf8-115"><strong>Long</strong></span></span></p></td>
<td><p><span data-ttu-id="73bf8-116">Uma constante como descrita em Comentários.</span><span class="sxs-lookup"><span data-stu-id="73bf8-116">A constant as described in Remarks.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73bf8-117"><em>Value</em></span><span class="sxs-lookup"><span data-stu-id="73bf8-117"><em>Value</em></span></span></p></td>
<td><p><span data-ttu-id="73bf8-118">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="73bf8-118">Required</span></span></p></td>
<td><p><span data-ttu-id="73bf8-119"><strong>Variantes</strong></span><span class="sxs-lookup"><span data-stu-id="73bf8-119"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="73bf8-120">O valor para o qual você deseja definir a opção.</span><span class="sxs-lookup"><span data-stu-id="73bf8-120">The value that you want to set option to.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="73bf8-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="73bf8-121">Remarks</span></span>

<span data-ttu-id="73bf8-122">Cada constante se refere à chave do Registro correspondente no caminho HKEY \_ LOCAL MACHINE SOFTWARE Microsoft Office \_ \\ \\ \\ \\ 12.0 \\ Access Connectivity \\ Engines ACE \\ (ou seja, **dbSharedAsyncDelay** corresponde à chave HKEY \_ LOCAL MACHINE SOFTWARE Microsoft Office \_ \\ \\ \\ \\ 12.0 \\ Access Connectivity \\ Engines ACE \\ \\ SharedAsyncDelay e assim por diante).</span><span class="sxs-lookup"><span data-stu-id="73bf8-122">Each constant refers to the corresponding registry key in the path HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Office\\12.0\\Access Connectivity Engine\\Engines\\ACE (that is, **dbSharedAsyncDelay** corresponds to the key HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Office\\12.0\\Access Connectivity Engine\\Engines\\ACE\\SharedAsyncDelay, and so on).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="73bf8-123">Constante</span><span class="sxs-lookup"><span data-stu-id="73bf8-123">Constant</span></span></p></th>
<th><p><span data-ttu-id="73bf8-124">Descrição</span><span class="sxs-lookup"><span data-stu-id="73bf8-124">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="73bf8-125"><strong>dbPageTimeout</strong></span><span class="sxs-lookup"><span data-stu-id="73bf8-125"><strong>dbPageTimeout</strong></span></span></p></td>
<td><p><span data-ttu-id="73bf8-126">A chave PageTimeout</span><span class="sxs-lookup"><span data-stu-id="73bf8-126">The PageTimeout key</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73bf8-127"><strong>dbSharedAsyncDelay</strong></span><span class="sxs-lookup"><span data-stu-id="73bf8-127"><strong>dbSharedAsyncDelay</strong></span></span></p></td>
<td><p><span data-ttu-id="73bf8-128">A chave SharedAsyncDelay</span><span class="sxs-lookup"><span data-stu-id="73bf8-128">The SharedAsyncDelay key</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73bf8-129"><strong>dbExclusiveAsyncDelay</strong></span><span class="sxs-lookup"><span data-stu-id="73bf8-129"><strong>dbExclusiveAsyncDelay</strong></span></span></p></td>
<td><p><span data-ttu-id="73bf8-130">A chave ExclusiveAsyncDelay</span><span class="sxs-lookup"><span data-stu-id="73bf8-130">The ExclusiveAsyncDelay key</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73bf8-131"><strong>dbLockRetry</strong></span><span class="sxs-lookup"><span data-stu-id="73bf8-131"><strong>dbLockRetry</strong></span></span></p></td>
<td><p><span data-ttu-id="73bf8-132">A chave LockRetry</span><span class="sxs-lookup"><span data-stu-id="73bf8-132">The LockRetry key</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73bf8-133"><strong>dbUserCommitSync</strong></span><span class="sxs-lookup"><span data-stu-id="73bf8-133"><strong>dbUserCommitSync</strong></span></span></p></td>
<td><p><span data-ttu-id="73bf8-134">A chave UserCommitSync</span><span class="sxs-lookup"><span data-stu-id="73bf8-134">The UserCommitSync key</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73bf8-135"><strong>dbImplicitCommitSync</strong></span><span class="sxs-lookup"><span data-stu-id="73bf8-135"><strong>dbImplicitCommitSync</strong></span></span></p></td>
<td><p><span data-ttu-id="73bf8-136">A chave ImplicitCommitSync</span><span class="sxs-lookup"><span data-stu-id="73bf8-136">The ImplicitCommitSync key</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73bf8-137"><strong>dbMaxBufferSize</strong></span><span class="sxs-lookup"><span data-stu-id="73bf8-137"><strong>dbMaxBufferSize</strong></span></span></p></td>
<td><p><span data-ttu-id="73bf8-138">A chave MaxBufferSize</span><span class="sxs-lookup"><span data-stu-id="73bf8-138">The MaxBufferSize key</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73bf8-139"><strong>dbMaxLocksPerFile</strong></span><span class="sxs-lookup"><span data-stu-id="73bf8-139"><strong>dbMaxLocksPerFile</strong></span></span></p></td>
<td><p><span data-ttu-id="73bf8-140">A chave MaxLocksPerFile</span><span class="sxs-lookup"><span data-stu-id="73bf8-140">The MaxLocksPerFile key</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73bf8-141"><strong>dbLockDelay</strong></span><span class="sxs-lookup"><span data-stu-id="73bf8-141"><strong>dbLockDelay</strong></span></span></p></td>
<td><p><span data-ttu-id="73bf8-142">A chave LockDelay</span><span class="sxs-lookup"><span data-stu-id="73bf8-142">The LockDelay key</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73bf8-143"><strong>dbRecycleLVs</strong></span><span class="sxs-lookup"><span data-stu-id="73bf8-143"><strong>dbRecycleLVs</strong></span></span></p></td>
<td><p><span data-ttu-id="73bf8-144">A chave RecycleLVs</span><span class="sxs-lookup"><span data-stu-id="73bf8-144">The RecycleLVs key</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73bf8-145"><strong>dbFlushTransactionTimeout</strong></span><span class="sxs-lookup"><span data-stu-id="73bf8-145"><strong>dbFlushTransactionTimeout</strong></span></span></p></td>
<td><p><span data-ttu-id="73bf8-146">A chave FlushTransactionTimeout</span><span class="sxs-lookup"><span data-stu-id="73bf8-146">The FlushTransactionTimeout key</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="73bf8-p101">Use o método **SetOption** para substituir os valores do Registro no tempo de execução. Novos valores estabelecidos com o método **SetOption** permanecem vigentes até que sejam alterados novamente por outra chamada **SetOption** ou até que o objeto **DBEngine** seja fechado.</span><span class="sxs-lookup"><span data-stu-id="73bf8-p101">Use the **SetOption** method to override registry values at run-time. New values established with the **SetOption** method remain in effect until changed again by another **SetOption** call, or until the **DBEngine** object is closed.</span></span>

