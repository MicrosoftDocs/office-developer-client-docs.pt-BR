---
title: Método Append (Colunas do ADOX)
TOCTitle: Append method (ADOX Columns)
ms:assetid: e256a478-abc0-f15b-fc29-1b52e354144a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250152(v=office.15)
ms:contentKeyID: 48548285
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 48bc100b7b56265a570ce963b80f569f1d827150
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297120"
---
# <a name="append-method-adox-columns"></a><span data-ttu-id="d2a59-102">Método Append (Colunas do ADOX)</span><span class="sxs-lookup"><span data-stu-id="d2a59-102">Append method (ADOX Columns)</span></span>

<span data-ttu-id="d2a59-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d2a59-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d2a59-104">Adiciona um novo objeto [Column](column-object-adox.md) à coleção [Columns](columns-collection-adox.md).</span><span class="sxs-lookup"><span data-stu-id="d2a59-104">Adds a new [Column](column-object-adox.md) object to the [Columns](columns-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2a59-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d2a59-105">Syntax</span></span>

<span data-ttu-id="d2a59-106">*Colunas*.</span><span class="sxs-lookup"><span data-stu-id="d2a59-106">*Columns*.</span></span> <span data-ttu-id="d2a59-107">Append *Column* \[ ,*Type* \] \[ ,*DefinedSize*\]</span><span class="sxs-lookup"><span data-stu-id="d2a59-107">Append *Column* \[,*Type*\] \[,*DefinedSize*\]</span></span>

## <a name="parameters"></a><span data-ttu-id="d2a59-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d2a59-108">Parameters</span></span>

|<span data-ttu-id="d2a59-109">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="d2a59-109">Parameter</span></span>|<span data-ttu-id="d2a59-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="d2a59-110">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="d2a59-111">*Column*</span><span class="sxs-lookup"><span data-stu-id="d2a59-111">*Column*</span></span> |<span data-ttu-id="d2a59-112">O objeto **Column** a ser anexado ou o nome da coluna a ser criada e anexada.</span><span class="sxs-lookup"><span data-stu-id="d2a59-112">The **Column** object to append or the name of the column to create and append.</span></span>|
|<span data-ttu-id="d2a59-113">*Type*</span><span class="sxs-lookup"><span data-stu-id="d2a59-113">*Type*</span></span> |<span data-ttu-id="d2a59-p102">Opcional. Um valor **Long** que especifica o tipo de dados da coluna. O parâmetro *Type* corresponde à propriedade [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-columnadox) de um objeto **Column**.</span><span class="sxs-lookup"><span data-stu-id="d2a59-p102">Optional. A **Long** value that specifies the data type of the column. The *Type* parameter corresponds to the [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-columnadox) property of a **Column** object.</span></span>|
|<span data-ttu-id="d2a59-117">*DefinedSize*</span><span class="sxs-lookup"><span data-stu-id="d2a59-117">*DefinedSize*</span></span> |<span data-ttu-id="d2a59-118">Opcional.</span><span class="sxs-lookup"><span data-stu-id="d2a59-118">Optional.</span></span> <span data-ttu-id="d2a59-119">Um valor **Long** que especifica o tamanho da coluna.</span><span class="sxs-lookup"><span data-stu-id="d2a59-119">A **Long** value that specifies the size of the column.</span></span> <span data-ttu-id="d2a59-120">O parâmetro *DefinedSize* corresponde à propriedade [DefinedSize](definedsize-property-adox.md) de um objeto **Column**.</span><span class="sxs-lookup"><span data-stu-id="d2a59-120">The *DefinedSize* parameter corresponds to the [DefinedSize](definedsize-property-adox.md) property of a **Column** object.</span></span>|


> [!NOTE]
> <span data-ttu-id="d2a59-121">Ocorrerá um erro ao anexar uma **Coluna** à coleção **Columns** de um [Índice](index-object-adox.md), se a **Coluna** não existir em uma [Tabela](table-object-adox.md) que já esteja anexada à coleção [Tables](tables-collection-adox.md).</span><span class="sxs-lookup"><span data-stu-id="d2a59-121">An error will occur when appending a **Column** to the **Columns** collection of an [Index](index-object-adox.md) if the **Column** does not exist in a [Table](table-object-adox.md) that is already appended to the [Tables](tables-collection-adox.md) collection.</span></span>


