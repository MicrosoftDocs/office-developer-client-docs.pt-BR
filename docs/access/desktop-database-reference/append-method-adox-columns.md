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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28711228"
---
# <a name="append-method-adox-columns"></a><span data-ttu-id="0605b-102">Método Append (Colunas do ADOX)</span><span class="sxs-lookup"><span data-stu-id="0605b-102">Append method (ADOX Columns)</span></span>

<span data-ttu-id="0605b-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="0605b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0605b-104">Adiciona um novo objeto [Column](column-object-adox.md) à coleção [Columns](columns-collection-adox.md).</span><span class="sxs-lookup"><span data-stu-id="0605b-104">Adds a new [Column](column-object-adox.md) object to the [Columns](columns-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="0605b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0605b-105">Syntax</span></span>

<span data-ttu-id="0605b-106">*Colunas*.</span><span class="sxs-lookup"><span data-stu-id="0605b-106">*Columns*.</span></span> <span data-ttu-id="0605b-107">Acrescentar*coluna* \[,*tipo* \] \[,*DefinedSize*\]</span><span class="sxs-lookup"><span data-stu-id="0605b-107">Append*Column* \[,*Type*\] \[,*DefinedSize*\]</span></span>

## <a name="parameters"></a><span data-ttu-id="0605b-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0605b-108">Parameters</span></span>

|<span data-ttu-id="0605b-109">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="0605b-109">Parameter</span></span>|<span data-ttu-id="0605b-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="0605b-110">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="0605b-111">*Column*</span><span class="sxs-lookup"><span data-stu-id="0605b-111">*Column*</span></span> |<span data-ttu-id="0605b-112">O objeto **Column** a ser anexado ou o nome da coluna a ser criada e anexada.</span><span class="sxs-lookup"><span data-stu-id="0605b-112">The **Column** object to append or the name of the column to create and append.</span></span>|
|<span data-ttu-id="0605b-113">*Type*</span><span class="sxs-lookup"><span data-stu-id="0605b-113">*Type*</span></span> |<span data-ttu-id="0605b-114">Opcional.</span><span class="sxs-lookup"><span data-stu-id="0605b-114">Optional.</span></span> <span data-ttu-id="0605b-115">Um valor **Long** que especifica o tipo de dados da coluna.</span><span class="sxs-lookup"><span data-stu-id="0605b-115">A **Long** value that specifies the data type of the column.</span></span> <span data-ttu-id="0605b-116">O parâmetro *Type* corresponde à propriedade [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-columnadox) de um objeto **Column** .</span><span class="sxs-lookup"><span data-stu-id="0605b-116">The *Type* parameter corresponds to the [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-columnadox) property of a **Column** object.</span></span>|
|<span data-ttu-id="0605b-117">*DefinedSize*</span><span class="sxs-lookup"><span data-stu-id="0605b-117">*DefinedSize*</span></span> |<span data-ttu-id="0605b-118">Opcional.</span><span class="sxs-lookup"><span data-stu-id="0605b-118">Optional.</span></span> <span data-ttu-id="0605b-119">Um valor **Long** que especifica o tamanho da coluna.</span><span class="sxs-lookup"><span data-stu-id="0605b-119">A **Long** value that specifies the size of the column.</span></span> <span data-ttu-id="0605b-120">O parâmetro *DefinedSize* corresponde à propriedade [DefinedSize](definedsize-property-adox.md) de um objeto **Column** .</span><span class="sxs-lookup"><span data-stu-id="0605b-120">The *DefinedSize* parameter corresponds to the [DefinedSize](definedsize-property-adox.md) property of a **Column** object.</span></span>|


> [!NOTE]
> <span data-ttu-id="0605b-121">[!OBSERVAçãO] Ocorrerá um erro ao anexar uma **Coluna** à coleção **Columns** de um [Índice](index-object-adox.md), se a **Coluna** não existir em uma [Tabela](table-object-adox.md) que já esteja anexada à coleção [Tables](tables-collection-adox.md).</span><span class="sxs-lookup"><span data-stu-id="0605b-121">An error will occur when appending a **Column** to the **Columns** collection of an [Index](index-object-adox.md) if the **Column** does not exist in a [Table](table-object-adox.md) that is already appended to the [Tables](tables-collection-adox.md) collection.</span></span>


