---
title: Método Database. Synchronize (DAO)
TOCTitle: Synchronize Method
ms:assetid: 5e716a4a-2430-8106-5c34-a02dd28bc4f6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194659(v=office.15)
ms:contentKeyID: 48545137
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053357
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 411948f3c0ac4d6c353cd2722136dffb6a25fb17
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294705"
---
# <a name="databasesynchronize-method-dao"></a><span data-ttu-id="baa83-102">Método Database. Synchronize (DAO)</span><span class="sxs-lookup"><span data-stu-id="baa83-102">Database.Synchronize method (DAO)</span></span>


<span data-ttu-id="baa83-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="baa83-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="baa83-104">Sincroniza duas réplicas.</span><span class="sxs-lookup"><span data-stu-id="baa83-104">Synchronizes two replicas.</span></span> <span data-ttu-id="baa83-105">(apenas espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="baa83-105">(Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="baa83-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="baa83-106">Syntax</span></span>

<span data-ttu-id="baa83-107">*expressão* . Sincronizar (***DbPathName***, ***ExchangeType***)</span><span class="sxs-lookup"><span data-stu-id="baa83-107">*expression* .Synchronize(***DbPathName***, ***ExchangeType***)</span></span>

<span data-ttu-id="baa83-108">*expressão* Uma variável que representa um objeto **Database** .</span><span class="sxs-lookup"><span data-stu-id="baa83-108">*expression* A variable that represents a **Database** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="baa83-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="baa83-109">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="baa83-110">Nome</span><span class="sxs-lookup"><span data-stu-id="baa83-110">Name</span></span></p></th>
<th><p><span data-ttu-id="baa83-111">Obrigatório/opcional</span><span class="sxs-lookup"><span data-stu-id="baa83-111">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="baa83-112">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="baa83-112">Data type</span></span></p></th>
<th><p><span data-ttu-id="baa83-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="baa83-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="baa83-114"><em>DbPathName</em></span><span class="sxs-lookup"><span data-stu-id="baa83-114"><em>DbPathName</em></span></span></p></td>
<td><p><span data-ttu-id="baa83-115">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="baa83-115">Required</span></span></p></td>
<td><p><span data-ttu-id="baa83-116"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="baa83-116"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="baa83-117">O caminho para a réplica de destino com a qual o banco de dados será sincronizado.</span><span class="sxs-lookup"><span data-stu-id="baa83-117">The path to the target replica with which database will be synchronized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baa83-118"><em>Servidor de troca</em></span><span class="sxs-lookup"><span data-stu-id="baa83-118"><em>ExchangeType</em></span></span></p></td>
<td><p><span data-ttu-id="baa83-119">Opcional</span><span class="sxs-lookup"><span data-stu-id="baa83-119">Optional</span></span></p></td>
<td><p><span data-ttu-id="baa83-120"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="baa83-120"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="baa83-121">Uma constante <strong><a href="synchronizetypeenum-enumeration-dao.md">SynchronizeTypeEnum</a></strong> que indica qual direção sincronizar as alterações entre os dois bancos de dados.</span><span class="sxs-lookup"><span data-stu-id="baa83-121">A <strong><a href="synchronizetypeenum-enumeration-dao.md">SynchronizeTypeEnum</a></strong> constant indicating which direction to synchronize changes between the two databases.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="baa83-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="baa83-122">Remarks</span></span>

<span data-ttu-id="baa83-123">Utilize **Synchronize** para trocar dados e alterações de design entre os dois bancos de dados.</span><span class="sxs-lookup"><span data-stu-id="baa83-123">You use **Synchronize** to exchange data and design changes between two databases.</span></span> <span data-ttu-id="baa83-124">As alterações de design sempre ocorrem primeiro.</span><span class="sxs-lookup"><span data-stu-id="baa83-124">Design changes always happen first.</span></span> <span data-ttu-id="baa83-125">Ambos os bancos de dados devem estar no mesmo nível de design antes de poderem trocar dados.</span><span class="sxs-lookup"><span data-stu-id="baa83-125">Both databases must be at the same design level before they can exchange data.</span></span> <span data-ttu-id="baa83-126">Por exemplo, uma troca do tipo **dbRepExportChanges** pode causar alterações de design em uma réplica, mesmo que as alterações de dados fluam somente do banco de dados para o DbPathName.</span><span class="sxs-lookup"><span data-stu-id="baa83-126">For example, an exchange of type **dbRepExportChanges** might cause design changes at a replica even though data changes flow only from the database to DbPathName.</span></span>

<span data-ttu-id="baa83-127">A réplica identificada no DbPathName deve fazer parte do mesmo conjunto de réplicas.</span><span class="sxs-lookup"><span data-stu-id="baa83-127">The replica identified in DbPathName must be part of the same replica set.</span></span> <span data-ttu-id="baa83-128">Se ambas as réplicas tiverem a mesma configuração da propriedade **ReplicaID** ou forem Estruturas-mestres para dois conjuntos diferentes de réplica, a sincronização falhará.</span><span class="sxs-lookup"><span data-stu-id="baa83-128">If both replicas have the same **ReplicaID** property setting or are Design Masters for two different replica sets, the synchronization fails.</span></span>

<span data-ttu-id="baa83-129">Ao sincronizar duas réplicas na Internet, você deve usar a constante **dbRepSyncInternet**.</span><span class="sxs-lookup"><span data-stu-id="baa83-129">When you synchronize two replicas over the Internet, you must use the **dbRepSyncInternet** constant.</span></span> <span data-ttu-id="baa83-130">Nesse caso, você especifica um endereço de URL (Uniform Resource Locator) para o argumento DbPathName em vez de especificar um caminho de rede de área local.</span><span class="sxs-lookup"><span data-stu-id="baa83-130">In this case, you specify a Uniform Resource Locator (URL) address for the DbPathName argument instead of specifying a local area network path.</span></span>


> [!NOTE]
> <span data-ttu-id="baa83-131">[!OBSERVAçãO] Não é possível sincronizar réplicas parciais com outras réplicas parciais.</span><span class="sxs-lookup"><span data-stu-id="baa83-131">You can't synchronize partial replicas with other partial replicas.</span></span> <span data-ttu-id="baa83-132">Consulte o método [PopulatePartial](database-populatepartial-method-dao.md) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="baa83-132">See the [PopulatePartial](database-populatepartial-method-dao.md) method for more information.</span></span>


