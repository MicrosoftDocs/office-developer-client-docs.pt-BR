---
title: Método Append (Índices do ADOX)
TOCTitle: Append Method (ADOX Indexes)
ms:assetid: 015ebab4-5e9d-8777-ac82-4d20e957c274
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248784(v=office.15)
ms:contentKeyID: 48542933
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5f91535075c2782861dc409a6c527f159cd5458a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462776"
---
# <a name="append-method-adox-indexes"></a><span data-ttu-id="3c360-102">Método Append (Índices do ADOX)</span><span class="sxs-lookup"><span data-stu-id="3c360-102">Append Method (ADOX Indexes)</span></span>


<span data-ttu-id="3c360-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="3c360-103">**Applies to**: Access 2013 | Office 2013</span></span>



<span data-ttu-id="3c360-104">Adiciona um novo objeto [Index](index-object-adox.md) à coleção [Indexes](indexes-collection-adox.md).</span><span class="sxs-lookup"><span data-stu-id="3c360-104">Adds a new [Index](index-object-adox.md) object to the [Indexes](indexes-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c360-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3c360-105">Syntax</span></span>

<span data-ttu-id="3c360-106">*Índices*. Acrescentar*índice* \[,*colunas*\]</span><span class="sxs-lookup"><span data-stu-id="3c360-106">*Indexes*.Append*Index* \[,*Columns*\]</span></span>

## <a name="parameters"></a><span data-ttu-id="3c360-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3c360-107">Parameters</span></span>

  - <span data-ttu-id="3c360-108">*Index*</span><span class="sxs-lookup"><span data-stu-id="3c360-108">*Index*</span></span>

  - <span data-ttu-id="3c360-109">O objeto **Index** a ser anexado ou o nome do índice a ser criado e anexado.</span><span class="sxs-lookup"><span data-stu-id="3c360-109">The **Index** object to append or the name of the index to create and append.</span></span>

  - <span data-ttu-id="3c360-110">*Columns*</span><span class="sxs-lookup"><span data-stu-id="3c360-110">*Columns*</span></span>

  - <span data-ttu-id="3c360-111">Opcional.</span><span class="sxs-lookup"><span data-stu-id="3c360-111">Optional.</span></span> <span data-ttu-id="3c360-112">Um valor **Variant** que especifica um ou mais nomes de colunas a serem indexadas.</span><span class="sxs-lookup"><span data-stu-id="3c360-112">A **Variant** value that specifies the name(s) of the column(s) to be indexed.</span></span> <span data-ttu-id="3c360-113">O parâmetro *Columns* corresponde aos valores da propriedade [Name](name-property-adox.md) de um objeto [Column](column-object-adox.md) ou objetos.</span><span class="sxs-lookup"><span data-stu-id="3c360-113">The *Columns* parameter corresponds to the value(s) of the [Name](name-property-adox.md) property of a [Column](column-object-adox.md) object or objects.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c360-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="3c360-114">Remarks</span></span>

<span data-ttu-id="3c360-115">O parâmetro *Columns* pode levar o nome de uma coluna ou uma matriz de nomes de coluna.</span><span class="sxs-lookup"><span data-stu-id="3c360-115">The *Columns* parameter can take either the name of a column or an array of column names.</span></span>

<span data-ttu-id="3c360-116">Ocorrerá um erro se o provedor não oferecer suporte para a criação de índices.</span><span class="sxs-lookup"><span data-stu-id="3c360-116">An error will occur if the provider does not support creating indexes.</span></span>

