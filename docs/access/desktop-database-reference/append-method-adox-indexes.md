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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297092"
---
# <a name="append-method-adox-indexes"></a><span data-ttu-id="93c48-102">Método Append (Índices do ADOX)</span><span class="sxs-lookup"><span data-stu-id="93c48-102">Append method (ADOX Indexes)</span></span>


<span data-ttu-id="93c48-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="93c48-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="93c48-104">Adiciona um novo objeto [Index](index-object-adox.md) à coleção [Indexes](indexes-collection-adox.md).</span><span class="sxs-lookup"><span data-stu-id="93c48-104">Adds a new [Index](index-object-adox.md) object to the [Indexes](indexes-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="93c48-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="93c48-105">Syntax</span></span>

<span data-ttu-id="93c48-106">*Índices*. Anexar*índice* \[,*colunas*\]</span><span class="sxs-lookup"><span data-stu-id="93c48-106">*Indexes*.Append*Index* \[,*Columns*\]</span></span>

## <a name="parameters"></a><span data-ttu-id="93c48-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="93c48-107">Parameters</span></span>

|<span data-ttu-id="93c48-108">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="93c48-108">Parameter</span></span>|<span data-ttu-id="93c48-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="93c48-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="93c48-110">*Índice*</span><span class="sxs-lookup"><span data-stu-id="93c48-110">*Index*</span></span> |<span data-ttu-id="93c48-111">O objeto **Index** a ser anexado ou o nome do índice a ser criado e anexado.</span><span class="sxs-lookup"><span data-stu-id="93c48-111">The **Index** object to append or the name of the index to create and append.</span></span>|
|<span data-ttu-id="93c48-112">*Columns*</span><span class="sxs-lookup"><span data-stu-id="93c48-112">*Columns*</span></span> |<span data-ttu-id="93c48-p101">Opcional. Um valor **Variant** que especifica um ou mais nomes de colunas a serem indexadas. O parâmetro *Columns* corresponde ao(s) valor(es) da propriedade [Name](name-property-adox.md) de um ou mais objetos [Column](column-object-adox.md).</span><span class="sxs-lookup"><span data-stu-id="93c48-p101">Optional. A **Variant** value that specifies the name(s) of the column(s) to be indexed. The *Columns* parameter corresponds to the value(s) of the [Name](name-property-adox.md) property of a [Column](column-object-adox.md) object or objects.</span></span>|

## <a name="remarks"></a><span data-ttu-id="93c48-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="93c48-116">Remarks</span></span>

<span data-ttu-id="93c48-117">O parâmetro *Columns* pode receber o nome de uma coluna ou uma matriz de nomes de colunas.</span><span class="sxs-lookup"><span data-stu-id="93c48-117">The *Columns* parameter can take either the name of a column or an array of column names.</span></span>

<span data-ttu-id="93c48-118">Ocorrerá um erro se o provedor não oferecer suporte para a criação de índices.</span><span class="sxs-lookup"><span data-stu-id="93c48-118">An error will occur if the provider does not support creating indexes.</span></span>

