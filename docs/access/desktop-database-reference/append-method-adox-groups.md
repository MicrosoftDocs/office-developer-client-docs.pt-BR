---
title: Método Append (Grupos do ADOX)
TOCTitle: Append Method (ADOX Groups)
ms:assetid: c3245a24-55b8-3f3f-1c4a-43a119d84dc8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249954(v=office.15)
ms:contentKeyID: 48547567
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f08b1bdbde8cc276e94947c2bd62250320f646c5
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25888584"
---
# <a name="append-method-adox-groups"></a><span data-ttu-id="b7142-102">Método Append (Grupos do ADOX)</span><span class="sxs-lookup"><span data-stu-id="b7142-102">Append Method (ADOX Groups)</span></span>


<span data-ttu-id="b7142-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="b7142-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="b7142-104">Adiciona um novo objeto [Group](group-object-adox.md) à coleção [Groups](groups-collection-adox.md).</span><span class="sxs-lookup"><span data-stu-id="b7142-104">Adds a new [Group](group-object-adox.md) object to the [Groups](groups-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7142-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b7142-105">Syntax</span></span>

<span data-ttu-id="b7142-106">*Grupos*. Acrescentar um*grupo*</span><span class="sxs-lookup"><span data-stu-id="b7142-106">*Groups*.Append*Group*</span></span>

## <a name="parameters"></a><span data-ttu-id="b7142-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b7142-107">Parameters</span></span>

  - <span data-ttu-id="b7142-108">*Group*</span><span class="sxs-lookup"><span data-stu-id="b7142-108">*Group*</span></span>

  - <span data-ttu-id="b7142-109">O objeto **Group** a ser anexado ou o nome do grupo a ser criado e anexado.</span><span class="sxs-lookup"><span data-stu-id="b7142-109">The **Group** object to append or the name of the group to create and append.</span></span>

## <a name="remarks"></a><span data-ttu-id="b7142-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="b7142-110">Remarks</span></span>

<span data-ttu-id="b7142-p101">A coleção **Groups** de um [Catálogo](catalog-object-adox.md) representa todas as contas de grupo do catálogo. A coleção **Groups** de um [Usuário](user-object-adox.md) representa apenas o grupo ao qual o usuário pertence.</span><span class="sxs-lookup"><span data-stu-id="b7142-p101">The **Groups** collection of a [Catalog](catalog-object-adox.md) represents all of the catalog's group accounts. The **Groups** collection for a [User](user-object-adox.md) represents only the group to which the user belongs.</span></span>

<span data-ttu-id="b7142-113">Ocorrerá um erro se o provedor não oferecer suporte para a criação de grupos.</span><span class="sxs-lookup"><span data-stu-id="b7142-113">An error will occur if the provider does not support creating groups.</span></span>


> [!NOTE]
> <span data-ttu-id="b7142-114">[!OBSERVAçãO] Antes de um objeto **Group** ser anexado à coleção **Groups** de um objeto **User**, na coleção **Groups** do [Catálogo](name-property-adox.md) já deve existir um objeto **Group** com o mesmo **Nome** daquele a ser anexado.</span><span class="sxs-lookup"><span data-stu-id="b7142-114">Before appending a **Group** object to the **Groups** collection of a **User** object, a **Group** object with the same [Name](name-property-adox.md) as the one to be appended must already exist in the **Groups** collection of the **Catalog**.</span></span>


