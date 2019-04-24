---
title: Método Delete (coleções do ADOX)
TOCTitle: Delete method (ADOX Collections)
ms:assetid: bcf9b8dd-cc7a-c1f9-fd93-58694766c4d9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249909(v=office.15)
ms:contentKeyID: 48547423
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 54c67848d321125af44d9f5bf50f3aa582b043bb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294075"
---
# <a name="delete-method-adox-collections"></a><span data-ttu-id="0e975-102">Método Delete (coleções do ADOX)</span><span class="sxs-lookup"><span data-stu-id="0e975-102">Delete method (ADOX Collections)</span></span>

<span data-ttu-id="0e975-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0e975-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0e975-104">Remove um objeto de uma coleção.</span><span class="sxs-lookup"><span data-stu-id="0e975-104">Removes an object from a collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e975-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0e975-105">Syntax</span></span>

<span data-ttu-id="0e975-106">*Coleção*. Excluir*nome*</span><span class="sxs-lookup"><span data-stu-id="0e975-106">*Collection*.Delete*Name*</span></span>

## <a name="parameters"></a><span data-ttu-id="0e975-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0e975-107">Parameters</span></span>

|<span data-ttu-id="0e975-108">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="0e975-108">Parameter</span></span>|<span data-ttu-id="0e975-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="0e975-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="0e975-110">*Name*</span><span class="sxs-lookup"><span data-stu-id="0e975-110">*Name*</span></span> |<span data-ttu-id="0e975-111">Um **Variant** que especifica o nome ou a posição ordinal (índice) do objeto a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="0e975-111">A **Variant** that specifies the name or ordinal position (index) of the object to delete.</span></span>|

## <a name="remarks"></a><span data-ttu-id="0e975-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="0e975-112">Remarks</span></span>

<span data-ttu-id="0e975-113">Ocorrerá um erro se o *Nome* não existir na coleção.</span><span class="sxs-lookup"><span data-stu-id="0e975-113">An error will occur if the *Name* does not exist in the collection.</span></span>

<span data-ttu-id="0e975-p101">Para as coleções [Tables](tables-collection-adox.md) e [Users](users-collection-adox.md), ocorrerá um erro se o provedor não oferecer suporte para a exclusão de tabelas ou usuários, respectivamente. Para as coleções [Procedures](procedures-collection-adox.md) e [Views](views-collection-adox.md), o comando **Delete** falhará se o provedor não oferecer suporte para comandos persistentes.</span><span class="sxs-lookup"><span data-stu-id="0e975-p101">For [Tables](tables-collection-adox.md) and [Users](users-collection-adox.md) collections, an error will occur if the provider does not support deleting tables or users, respectively. For [Procedures](procedures-collection-adox.md) and [Views](views-collection-adox.md) collections, **Delete** will fail if the provider does not support persisting commands.</span></span>

