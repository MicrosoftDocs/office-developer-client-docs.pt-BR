---
title: Método Append (Índices do ADOX)
TOCTitle: Append method (ADOX Indexes)
ms:assetid: 015ebab4-5e9d-8777-ac82-4d20e957c274
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248784(v=office.15)
ms:contentKeyID: 48542933
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 00a02e74bbbc1b24939784a89965bf0757be0cfe
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949401"
---
# <a name="append-method-adox-indexes"></a><span data-ttu-id="a3717-102">Método Append (Índices do ADOX)</span><span class="sxs-lookup"><span data-stu-id="a3717-102">Append method (ADOX Indexes)</span></span>


<span data-ttu-id="a3717-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="a3717-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="a3717-104">Adiciona um novo objeto [Index](index-object-adox.md) à coleção [Indexes](indexes-collection-adox.md).</span><span class="sxs-lookup"><span data-stu-id="a3717-104">Adds a new [Index](index-object-adox.md) object to the [Indexes](indexes-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3717-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a3717-105">Syntax</span></span>

<span data-ttu-id="a3717-106">*Índices*. Acrescentar*índice* \[,*colunas*\]</span><span class="sxs-lookup"><span data-stu-id="a3717-106">*Indexes*.Append*Index* \[,*Columns*\]</span></span>

## <a name="parameters"></a><span data-ttu-id="a3717-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a3717-107">Parameters</span></span>

|<span data-ttu-id="a3717-108">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="a3717-108">Parameter</span></span>|<span data-ttu-id="a3717-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="a3717-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="a3717-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="a3717-110">*Index*</span></span> |<span data-ttu-id="a3717-111">O objeto **Index** a ser anexado ou o nome do índice a ser criado e anexado.</span><span class="sxs-lookup"><span data-stu-id="a3717-111">The **Index** object to append or the name of the index to create and append.</span></span>|
|<span data-ttu-id="a3717-112">*Columns*</span><span class="sxs-lookup"><span data-stu-id="a3717-112">*Columns*</span></span> |<span data-ttu-id="a3717-113">Opcional.</span><span class="sxs-lookup"><span data-stu-id="a3717-113">Optional.</span></span> <span data-ttu-id="a3717-114">Um valor **Variant** que especifica um ou mais nomes de colunas a serem indexadas.</span><span class="sxs-lookup"><span data-stu-id="a3717-114">A **Variant** value that specifies the name(s) of the column(s) to be indexed.</span></span> <span data-ttu-id="a3717-115">O parâmetro *Columns* corresponde aos valores da propriedade [Name](name-property-adox.md) de um objeto [Column](column-object-adox.md) ou objetos.</span><span class="sxs-lookup"><span data-stu-id="a3717-115">The *Columns* parameter corresponds to the value(s) of the [Name](name-property-adox.md) property of a [Column](column-object-adox.md) object or objects.</span></span>|

## <a name="remarks"></a><span data-ttu-id="a3717-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="a3717-116">Remarks</span></span>

<span data-ttu-id="a3717-117">O parâmetro *Columns* pode levar o nome de uma coluna ou uma matriz de nomes de coluna.</span><span class="sxs-lookup"><span data-stu-id="a3717-117">The *Columns* parameter can take either the name of a column or an array of column names.</span></span>

<span data-ttu-id="a3717-118">Ocorrerá um erro se o provedor não oferecer suporte para a criação de índices.</span><span class="sxs-lookup"><span data-stu-id="a3717-118">An error will occur if the provider does not support creating indexes.</span></span>

