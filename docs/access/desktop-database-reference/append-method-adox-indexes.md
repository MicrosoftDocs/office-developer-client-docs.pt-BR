---
title: Método Append (Índices do ADOX)
TOCTitle: Append method (ADOX Indexes)
ms:assetid: 015ebab4-5e9d-8777-ac82-4d20e957c274
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248784(v=office.15)
ms:contentKeyID: 48542933
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0b541512de9748e94d033bb56f27dd0941c7f5a7
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28707553"
---
# <a name="append-method-adox-indexes"></a><span data-ttu-id="2df15-102">Método Append (Índices do ADOX)</span><span class="sxs-lookup"><span data-stu-id="2df15-102">Append method (ADOX Indexes)</span></span>


<span data-ttu-id="2df15-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="2df15-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="2df15-104">Adiciona um novo objeto [Index](index-object-adox.md) à coleção [Indexes](indexes-collection-adox.md).</span><span class="sxs-lookup"><span data-stu-id="2df15-104">Adds a new [Index](index-object-adox.md) object to the [Indexes](indexes-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="2df15-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2df15-105">Syntax</span></span>

<span data-ttu-id="2df15-106">*Índices*. Acrescentar*índice* \[,*colunas*\]</span><span class="sxs-lookup"><span data-stu-id="2df15-106">*Indexes*.Append*Index* \[,*Columns*\]</span></span>

## <a name="parameters"></a><span data-ttu-id="2df15-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2df15-107">Parameters</span></span>

|<span data-ttu-id="2df15-108">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="2df15-108">Parameter</span></span>|<span data-ttu-id="2df15-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="2df15-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="2df15-110">*Índice*</span><span class="sxs-lookup"><span data-stu-id="2df15-110">*Index*</span></span> |<span data-ttu-id="2df15-111">O objeto **Index** a ser anexado ou o nome do índice a ser criado e anexado.</span><span class="sxs-lookup"><span data-stu-id="2df15-111">The **Index** object to append or the name of the index to create and append.</span></span>|
|<span data-ttu-id="2df15-112">*Columns*</span><span class="sxs-lookup"><span data-stu-id="2df15-112">*Columns*</span></span> |<span data-ttu-id="2df15-113">Opcional.</span><span class="sxs-lookup"><span data-stu-id="2df15-113">Optional.</span></span> <span data-ttu-id="2df15-114">Um valor **Variant** que especifica um ou mais nomes de colunas a serem indexadas.</span><span class="sxs-lookup"><span data-stu-id="2df15-114">A **Variant** value that specifies the name(s) of the column(s) to be indexed.</span></span> <span data-ttu-id="2df15-115">O parâmetro *Columns* corresponde aos valores da propriedade [Name](name-property-adox.md) de um objeto [Column](column-object-adox.md) ou objetos.</span><span class="sxs-lookup"><span data-stu-id="2df15-115">The *Columns* parameter corresponds to the value(s) of the [Name](name-property-adox.md) property of a [Column](column-object-adox.md) object or objects.</span></span>|

## <a name="remarks"></a><span data-ttu-id="2df15-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="2df15-116">Remarks</span></span>

<span data-ttu-id="2df15-117">O parâmetro *Columns* pode levar o nome de uma coluna ou uma matriz de nomes de coluna.</span><span class="sxs-lookup"><span data-stu-id="2df15-117">The *Columns* parameter can take either the name of a column or an array of column names.</span></span>

<span data-ttu-id="2df15-118">Ocorrerá um erro se o provedor não oferecer suporte para a criação de índices.</span><span class="sxs-lookup"><span data-stu-id="2df15-118">An error will occur if the provider does not support creating indexes.</span></span>

