---
title: Método DBEngine (DAO)
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
ms.openlocfilehash: 1d11d9c6e3434e635d93e9c499c6d5f7c82c6f49
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867864"
---
# <a name="dbenginesetoption-method-dao"></a><span data-ttu-id="b31dc-102">Método DBEngine (DAO)</span><span class="sxs-lookup"><span data-stu-id="b31dc-102">DBEngine.SetOption Method (DAO)</span></span>


<span data-ttu-id="b31dc-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="b31dc-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b31dc-104">Substitui temporariamente os valores para as chaves do mecanismo de banco de dados do Microsoft Access no Registro do Windows (somente espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="b31dc-104">Temporarily overrides values for the Microsoft Access database engine keys in the Windows Registry (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="b31dc-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b31dc-105">Syntax</span></span>

<span data-ttu-id="b31dc-106">*expressão* . SetOption (***opção***, o ***valor***)</span><span class="sxs-lookup"><span data-stu-id="b31dc-106">*expression* .SetOption(***Option***, ***Value***)</span></span>

<span data-ttu-id="b31dc-107">*expressão* Uma expressão que retorna um objeto **DBEngine** .</span><span class="sxs-lookup"><span data-stu-id="b31dc-107">*expression* An expression that returns a **DBEngine** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="b31dc-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b31dc-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b31dc-109">Nome</span><span class="sxs-lookup"><span data-stu-id="b31dc-109">Name</span></span></p></th>
<th><p><span data-ttu-id="b31dc-110">Obrigatório/Opcional</span><span class="sxs-lookup"><span data-stu-id="b31dc-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="b31dc-111">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="b31dc-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="b31dc-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="b31dc-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b31dc-113">Opção</span><span class="sxs-lookup"><span data-stu-id="b31dc-113">Option</span></span></p></td>
<td><p><span data-ttu-id="b31dc-114">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="b31dc-114">Required</span></span></p></td>
<td><p><span data-ttu-id="b31dc-115"><strong>Long</strong></span><span class="sxs-lookup"><span data-stu-id="b31dc-115"><strong>Long</strong></span></span></p></td>
<td><p><span data-ttu-id="b31dc-116">Uma constante como descrita em Comentários.</span><span class="sxs-lookup"><span data-stu-id="b31dc-116">A constant as described in Remarks.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b31dc-117">Valor</span><span class="sxs-lookup"><span data-stu-id="b31dc-117">Value</span></span></p></td>
<td><p><span data-ttu-id="b31dc-118">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="b31dc-118">Required</span></span></p></td>
<td><p><span data-ttu-id="b31dc-119"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="b31dc-119"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="b31dc-120">O valor que você deseja definir para option.</span><span class="sxs-lookup"><span data-stu-id="b31dc-120">The value that you want to set option to.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="b31dc-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="b31dc-121">Remarks</span></span>

<span data-ttu-id="b31dc-122">Cada constante refere-se a chave do registro correspondente no caminho HKEY\_LOCAL\_máquina\\SOFTWARE\\Microsoft\\Office\\12.0\\mecanismo de conectividade do Access\\mecanismos\\bem (ou seja, **dbSharedAsyncDelay** corresponde à tecla HKEY\_LOCAL\_máquina\\SOFTWARE\\Microsoft\\Office\\12.0\\mecanismo de conectividade do Access\\mecanismos\\ACE \\SharedAsyncDelay, e assim por diante).</span><span class="sxs-lookup"><span data-stu-id="b31dc-122">Each constant refers to the corresponding registry key in the path HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Office\\12.0\\Access Connectivity Engine\\Engines\\ACE (that is, **dbSharedAsyncDelay** corresponds to the key HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Office\\12.0\\Access Connectivity Engine\\Engines\\ACE\\SharedAsyncDelay, and so on).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b31dc-123">Constant</span><span class="sxs-lookup"><span data-stu-id="b31dc-123">Constant</span></span></p></th>
<th><p><span data-ttu-id="b31dc-124">Descrição</span><span class="sxs-lookup"><span data-stu-id="b31dc-124">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b31dc-125"><strong>dbPageTimeout</strong></span><span class="sxs-lookup"><span data-stu-id="b31dc-125"><strong>dbPageTimeout</strong></span></span></p></td>
<td><p><span data-ttu-id="b31dc-126">A chave PageTimeout</span><span class="sxs-lookup"><span data-stu-id="b31dc-126">The PageTimeout key</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b31dc-127"><strong>dbSharedAsyncDelay</strong></span><span class="sxs-lookup"><span data-stu-id="b31dc-127"><strong>dbSharedAsyncDelay</strong></span></span></p></td>
<td><p><span data-ttu-id="b31dc-128">A chave SharedAsyncDelay</span><span class="sxs-lookup"><span data-stu-id="b31dc-128">The SharedAsyncDelay key</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b31dc-129"><strong>dbExclusiveAsyncDelay</strong></span><span class="sxs-lookup"><span data-stu-id="b31dc-129"><strong>dbExclusiveAsyncDelay</strong></span></span></p></td>
<td><p><span data-ttu-id="b31dc-130">A chave ExclusiveAsyncDelay</span><span class="sxs-lookup"><span data-stu-id="b31dc-130">The ExclusiveAsyncDelay key</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b31dc-131"><strong>dbLockRetry</strong></span><span class="sxs-lookup"><span data-stu-id="b31dc-131"><strong>dbLockRetry</strong></span></span></p></td>
<td><p><span data-ttu-id="b31dc-132">A chave LockRetry</span><span class="sxs-lookup"><span data-stu-id="b31dc-132">The LockRetry key</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b31dc-133"><strong>dbUserCommitSync</strong></span><span class="sxs-lookup"><span data-stu-id="b31dc-133"><strong>dbUserCommitSync</strong></span></span></p></td>
<td><p><span data-ttu-id="b31dc-134">A chave UserCommitSync</span><span class="sxs-lookup"><span data-stu-id="b31dc-134">The UserCommitSync key</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b31dc-135"><strong>dbImplicitCommitSync</strong></span><span class="sxs-lookup"><span data-stu-id="b31dc-135"><strong>dbImplicitCommitSync</strong></span></span></p></td>
<td><p><span data-ttu-id="b31dc-136">A chave ImplicitCommitSync</span><span class="sxs-lookup"><span data-stu-id="b31dc-136">The ImplicitCommitSync key</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b31dc-137"><strong>dbMaxBufferSize</strong></span><span class="sxs-lookup"><span data-stu-id="b31dc-137"><strong>dbMaxBufferSize</strong></span></span></p></td>
<td><p><span data-ttu-id="b31dc-138">A chave MaxBufferSize</span><span class="sxs-lookup"><span data-stu-id="b31dc-138">The MaxBufferSize key</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b31dc-139"><strong>dbMaxLocksPerFile</strong></span><span class="sxs-lookup"><span data-stu-id="b31dc-139"><strong>dbMaxLocksPerFile</strong></span></span></p></td>
<td><p><span data-ttu-id="b31dc-140">A chave MaxLocksPerFile</span><span class="sxs-lookup"><span data-stu-id="b31dc-140">The MaxLocksPerFile key</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b31dc-141"><strong>dbLockDelay</strong></span><span class="sxs-lookup"><span data-stu-id="b31dc-141"><strong>dbLockDelay</strong></span></span></p></td>
<td><p><span data-ttu-id="b31dc-142">A chave LockDelay</span><span class="sxs-lookup"><span data-stu-id="b31dc-142">The LockDelay key</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b31dc-143"><strong>dbRecycleLVs</strong></span><span class="sxs-lookup"><span data-stu-id="b31dc-143"><strong>dbRecycleLVs</strong></span></span></p></td>
<td><p><span data-ttu-id="b31dc-144">A chave RecycleLVs</span><span class="sxs-lookup"><span data-stu-id="b31dc-144">The RecycleLVs key</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b31dc-145"><strong>dbFlushTransactionTimeout</strong></span><span class="sxs-lookup"><span data-stu-id="b31dc-145"><strong>dbFlushTransactionTimeout</strong></span></span></p></td>
<td><p><span data-ttu-id="b31dc-146">A chave FlushTransactionTimeout</span><span class="sxs-lookup"><span data-stu-id="b31dc-146">The FlushTransactionTimeout key</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b31dc-p101">Use o método **SetOption** para substituir os valores do Registro no tempo de execução. Novos valores estabelecidos com o método **SetOption** permanecem vigentes até que sejam alterados novamente por outra chamada **SetOption** ou até que o objeto **DBEngine** seja fechado.</span><span class="sxs-lookup"><span data-stu-id="b31dc-p101">Use the **SetOption** method to override registry values at run-time. New values established with the **SetOption** method remain in effect until changed again by another **SetOption** call, or until the **DBEngine** object is closed.</span></span>

