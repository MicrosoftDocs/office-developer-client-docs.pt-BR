---
title: Método Database.Synchronize (DAO)
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
ms.openlocfilehash: c55eab611cae8431a3ff3f2220cdfa8b1923d891
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463652"
---
# <a name="databasesynchronize-method-dao"></a><span data-ttu-id="0f097-102">Método Database.Synchronize (DAO)</span><span class="sxs-lookup"><span data-stu-id="0f097-102">Database.Synchronize Method (DAO)</span></span>


<span data-ttu-id="0f097-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="0f097-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="0f097-p101">Sincroniza duas réplicas. (apenas espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="0f097-p101">Synchronizes two replicas. (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="0f097-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0f097-106">Syntax</span></span>

<span data-ttu-id="0f097-107">*expressão* . Sincronizar (***DbPathName***, ***ExchangeType***)</span><span class="sxs-lookup"><span data-stu-id="0f097-107">*expression* .Synchronize(***DbPathName***, ***ExchangeType***)</span></span>

<span data-ttu-id="0f097-108">*expressão* Uma variável que representa um objeto de **banco de dados** .</span><span class="sxs-lookup"><span data-stu-id="0f097-108">*expression* A variable that represents a **Database** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="0f097-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0f097-109">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0f097-110">Nome</span><span class="sxs-lookup"><span data-stu-id="0f097-110">Name</span></span></p></th>
<th><p><span data-ttu-id="0f097-111">Obrigatório/Opcional</span><span class="sxs-lookup"><span data-stu-id="0f097-111">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="0f097-112">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="0f097-112">Data Type</span></span></p></th>
<th><p><span data-ttu-id="0f097-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="0f097-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0f097-114">DbPathName</span><span class="sxs-lookup"><span data-stu-id="0f097-114">DbPathName</span></span></p></td>
<td><p><span data-ttu-id="0f097-115">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="0f097-115">Required</span></span></p></td>
<td><p><span data-ttu-id="0f097-116"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="0f097-116"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="0f097-117">O caminho para a réplica de destino com a qual o banco de dados será sincronizado.</span><span class="sxs-lookup"><span data-stu-id="0f097-117">The path to the target replica with which database will be synchronized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0f097-118">ExchangeType</span><span class="sxs-lookup"><span data-stu-id="0f097-118">ExchangeType</span></span></p></td>
<td><p><span data-ttu-id="0f097-119">Opcional</span><span class="sxs-lookup"><span data-stu-id="0f097-119">Optional</span></span></p></td>
<td><p><span data-ttu-id="0f097-120"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="0f097-120"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="0f097-121">Uma constante <strong><a href="synchronizetypeenum-enumeration-dao.md">SynchronizeTypeEnum</a></strong> indicando a direção para sincronização das alterações entre os dois bancos de dados.</span><span class="sxs-lookup"><span data-stu-id="0f097-121">A <strong><a href="synchronizetypeenum-enumeration-dao.md">SynchronizeTypeEnum</a></strong> constant indicating which direction to synchronize changes between the two databases.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="0f097-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="0f097-122">Remarks</span></span>

<span data-ttu-id="0f097-123">Utilize **Synchronize** para trocar dados e alterações de design entre os dois bancos de dados.</span><span class="sxs-lookup"><span data-stu-id="0f097-123">You use **Synchronize** to exchange data and design changes between two databases.</span></span> <span data-ttu-id="0f097-124">As alterações de design sempre ocorrem primeiro.</span><span class="sxs-lookup"><span data-stu-id="0f097-124">Design changes always happen first.</span></span> <span data-ttu-id="0f097-125">Ambos os bancos de dados devem estar no mesmo nível de design antes de poderem trocar dados.</span><span class="sxs-lookup"><span data-stu-id="0f097-125">Both databases must be at the same design level before they can exchange data.</span></span> <span data-ttu-id="0f097-126">Por exemplo, uma troca de tipo **dbRepExportChanges** pode causar alterações de design em uma réplica, mesmo que as alterações de dados fluxo apenas do banco de dados em DbPathName.</span><span class="sxs-lookup"><span data-stu-id="0f097-126">For example, an exchange of type **dbRepExportChanges** might cause design changes at a replica even though data changes flow only from the database to DbPathName.</span></span>

<span data-ttu-id="0f097-127">A réplica identificada no DbPathName deve fazer parte do mesmo conjunto de réplicas.</span><span class="sxs-lookup"><span data-stu-id="0f097-127">The replica identified in DbPathName must be part of the same replica set.</span></span> <span data-ttu-id="0f097-128">Se ambas as réplicas tiverem a mesma configuração da propriedade **ReplicaID** ou forem Estruturas-mestres para dois conjuntos diferentes de réplica, a sincronização falhará.</span><span class="sxs-lookup"><span data-stu-id="0f097-128">If both replicas have the same **ReplicaID** property setting or are Design Masters for two different replica sets, the synchronization fails.</span></span>

<span data-ttu-id="0f097-129">Ao sincronizar duas réplicas na Internet, você deve usar a constante **dbRepSyncInternet**.</span><span class="sxs-lookup"><span data-stu-id="0f097-129">When you synchronize two replicas over the Internet, you must use the **dbRepSyncInternet** constant.</span></span> <span data-ttu-id="0f097-130">Nesse caso, você pode especificar um endereço de Uniform Resource Locator (URL) para o argumento DbPathName em vez de especificar um caminho de rede local.</span><span class="sxs-lookup"><span data-stu-id="0f097-130">In this case, you specify a Uniform Resource Locator (URL) address for the DbPathName argument instead of specifying a local area network path.</span></span>


> [!NOTE]
> <P><span data-ttu-id="0f097-p105">[!OBSERVAçãO] Não é possível sincronizar réplicas parciais com outras réplicas parciais. Consulte o método <STRONG><A href="database-populatepartial-method-dao.md">PopulatePartial</A></STRONG> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="0f097-p105">You can't synchronize partial replicas with other partial replicas. See the <STRONG><A href="database-populatepartial-method-dao.md">PopulatePartial</A></STRONG> method for more information.</span></span></P>


