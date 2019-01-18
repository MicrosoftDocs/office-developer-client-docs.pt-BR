---
title: Método Append (Chaves do ADOX)
TOCTitle: Append method (ADOX Keys)
ms:assetid: 14d6e8d7-5c9e-a422-47d6-ebfd9dd7a120
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248913(v=office.15)
ms:contentKeyID: 48543396
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c301f6809ab7f785497637b12e0b5d7a0bb7772d
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718900"
---
# <a name="append-method-adox-keys"></a><span data-ttu-id="83771-102">Método Append (Chaves do ADOX)</span><span class="sxs-lookup"><span data-stu-id="83771-102">Append method (ADOX Keys)</span></span>

<span data-ttu-id="83771-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="83771-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="83771-104">Adiciona um novo objeto [Key](key-object-adox.md) à coleção [Keys](keys-collection-adox.md).</span><span class="sxs-lookup"><span data-stu-id="83771-104">Adds a new [Key](key-object-adox.md) object to the [Keys](keys-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="83771-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="83771-105">Syntax</span></span>

<span data-ttu-id="83771-106">*Chaves*. Acrescentar*chave* \[,*KeyType* \] \[,*coluna* \] \[,*RelatedTable* \] \[,*RelatedColumn*\]</span><span class="sxs-lookup"><span data-stu-id="83771-106">*Keys*.Append*Key* \[,*KeyType*\] \[,*Column*\] \[,*RelatedTable*\] \[,*RelatedColumn*\]</span></span>

## <a name="parameters"></a><span data-ttu-id="83771-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="83771-107">Parameters</span></span>

|<span data-ttu-id="83771-108">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="83771-108">Parameter</span></span>|<span data-ttu-id="83771-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="83771-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="83771-110">*Tecla*</span><span class="sxs-lookup"><span data-stu-id="83771-110">*Key*</span></span> |<span data-ttu-id="83771-111">O objeto **Key** a ser anexado ou o nome da chave a ser criada e anexada.</span><span class="sxs-lookup"><span data-stu-id="83771-111">The **Key** object to append or the name of the key to create and append.</span></span>|
|<span data-ttu-id="83771-112">*KeyType*</span><span class="sxs-lookup"><span data-stu-id="83771-112">*KeyType*</span></span> |<span data-ttu-id="83771-113">Opcional.</span><span class="sxs-lookup"><span data-stu-id="83771-113">Optional.</span></span> <span data-ttu-id="83771-114">Um valor **Long** que especifica o tipo de chave.</span><span class="sxs-lookup"><span data-stu-id="83771-114">A **Long** value that specifies the type of key.</span></span> <span data-ttu-id="83771-115">O parâmetro *Key* corresponde à propriedade [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-keyadox) de um objeto **Key** .</span><span class="sxs-lookup"><span data-stu-id="83771-115">The *Key* parameter corresponds to the [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-keyadox) property of a **Key** object.</span></span>|
|<span data-ttu-id="83771-116">*Column*</span><span class="sxs-lookup"><span data-stu-id="83771-116">*Column*</span></span> |<span data-ttu-id="83771-117">Opcional.</span><span class="sxs-lookup"><span data-stu-id="83771-117">Optional.</span></span> <span data-ttu-id="83771-118">Um valor **String** que especifica o nome da coluna a ser indexada.</span><span class="sxs-lookup"><span data-stu-id="83771-118">A **String** value that specifies the name of the column to be indexed.</span></span> <span data-ttu-id="83771-119">O parâmetro *Columns* corresponde ao valor da propriedade [Name](name-property-adox.md) de um objeto [Column](column-object-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="83771-119">The *Columns* parameter corresponds to the value of the [Name](name-property-adox.md) property of a [Column](column-object-adox.md) object.</span></span>|
|<span data-ttu-id="83771-120">*RelatedTable*</span><span class="sxs-lookup"><span data-stu-id="83771-120">*RelatedTable*</span></span> |<span data-ttu-id="83771-121">Opcional.</span><span class="sxs-lookup"><span data-stu-id="83771-121">Optional.</span></span> <span data-ttu-id="83771-122">Um valor **String** que especifica o nome da tabela relacionada.</span><span class="sxs-lookup"><span data-stu-id="83771-122">A **String** value that specifies the name of the related table.</span></span> <span data-ttu-id="83771-123">O parâmetro *RelatedTable* corresponde ao valor da propriedade **Name** de um objeto [Table](table-object-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="83771-123">The *RelatedTable* parameter corresponds to the value of the **Name** property of a [Table](table-object-adox.md) object.</span></span>|
|<span data-ttu-id="83771-124">*RelatedColumn*</span><span class="sxs-lookup"><span data-stu-id="83771-124">*RelatedColumn*</span></span> |<span data-ttu-id="83771-p104">Opcional. Um valor **String** que especifica o nome da coluna relacionada para uma chave estrangeira. O parâmetro RelatedColumn corresponde ao valor da propriedade **Name** de um objeto **Column**.</span><span class="sxs-lookup"><span data-stu-id="83771-p104">Optional. A **String** value that specifies the name of the related column for a foreign key. The RelatedColumn parameter corresponds to the value of the **Name** property of a **Column** object.</span></span>|

## <a name="remarks"></a><span data-ttu-id="83771-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="83771-128">Remarks</span></span>

<span data-ttu-id="83771-129">O parâmetro *Columns* pode levar o nome de uma coluna ou uma matriz de nomes de coluna.</span><span class="sxs-lookup"><span data-stu-id="83771-129">The *Columns* parameter can take either the name of a column or an array of column names.</span></span>

