---
title: Método Append (Chaves do ADOX)
TOCTitle: Append Method (ADOX Keys)
ms:assetid: 14d6e8d7-5c9e-a422-47d6-ebfd9dd7a120
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248913(v=office.15)
ms:contentKeyID: 48543396
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5ba46c922ff9fc27da0abc1908f6ffaff8e997ef
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25879456"
---
# <a name="append-method-adox-keys"></a><span data-ttu-id="55bc1-102">Método Append (Chaves do ADOX)</span><span class="sxs-lookup"><span data-stu-id="55bc1-102">Append Method (ADOX Keys)</span></span>


<span data-ttu-id="55bc1-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="55bc1-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="55bc1-104">Adiciona um novo objeto [Key](key-object-adox.md) à coleção [Keys](keys-collection-adox.md).</span><span class="sxs-lookup"><span data-stu-id="55bc1-104">Adds a new [Key](key-object-adox.md) object to the [Keys](keys-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="55bc1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="55bc1-105">Syntax</span></span>

<span data-ttu-id="55bc1-106">*Chaves*. Acrescentar*chave* \[,*KeyType* \] \[,*coluna* \] \[,*RelatedTable* \] \[,*RelatedColumn*\]</span><span class="sxs-lookup"><span data-stu-id="55bc1-106">*Keys*.Append*Key* \[,*KeyType*\] \[,*Column*\] \[,*RelatedTable*\] \[,*RelatedColumn*\]</span></span>

## <a name="parameters"></a><span data-ttu-id="55bc1-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="55bc1-107">Parameters</span></span>

  - <span data-ttu-id="55bc1-108">*Key*</span><span class="sxs-lookup"><span data-stu-id="55bc1-108">*Key*</span></span>

  - <span data-ttu-id="55bc1-109">O objeto **Key** a ser anexado ou o nome da chave a ser criada e anexada.</span><span class="sxs-lookup"><span data-stu-id="55bc1-109">The **Key** object to append or the name of the key to create and append.</span></span>

  - <span data-ttu-id="55bc1-110">*KeyType*</span><span class="sxs-lookup"><span data-stu-id="55bc1-110">*KeyType*</span></span>

  - <span data-ttu-id="55bc1-111">Opcional.</span><span class="sxs-lookup"><span data-stu-id="55bc1-111">Optional.</span></span> <span data-ttu-id="55bc1-112">Um valor **Long** que especifica o tipo de chave.</span><span class="sxs-lookup"><span data-stu-id="55bc1-112">A **Long** value that specifies the type of key.</span></span> <span data-ttu-id="55bc1-113">O parâmetro *Key* corresponde à propriedade [Type](https://msdn.microsoft.com/library/jj248879\(v=office.15\)) de um objeto **Key** .</span><span class="sxs-lookup"><span data-stu-id="55bc1-113">The *Key* parameter corresponds to the [Type](https://msdn.microsoft.com/library/jj248879\(v=office.15\)) property of a **Key** object.</span></span>

  - <span data-ttu-id="55bc1-114">*Column*</span><span class="sxs-lookup"><span data-stu-id="55bc1-114">*Column*</span></span>

  - <span data-ttu-id="55bc1-115">Opcional.</span><span class="sxs-lookup"><span data-stu-id="55bc1-115">Optional.</span></span> <span data-ttu-id="55bc1-116">Um valor **String** que especifica o nome da coluna a ser indexada.</span><span class="sxs-lookup"><span data-stu-id="55bc1-116">A **String** value that specifies the name of the column to be indexed.</span></span> <span data-ttu-id="55bc1-117">O parâmetro *Columns* corresponde ao valor da propriedade [Name](name-property-adox.md) de um objeto [Column](column-object-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="55bc1-117">The *Columns* parameter corresponds to the value of the [Name](name-property-adox.md) property of a [Column](column-object-adox.md) object.</span></span>

  - <span data-ttu-id="55bc1-118">*RelatedTable*</span><span class="sxs-lookup"><span data-stu-id="55bc1-118">*RelatedTable*</span></span>

  - <span data-ttu-id="55bc1-119">Opcional.</span><span class="sxs-lookup"><span data-stu-id="55bc1-119">Optional.</span></span> <span data-ttu-id="55bc1-120">Um valor **String** que especifica o nome da tabela relacionada.</span><span class="sxs-lookup"><span data-stu-id="55bc1-120">A **String** value that specifies the name of the related table.</span></span> <span data-ttu-id="55bc1-121">O parâmetro *RelatedTable* corresponde ao valor da propriedade **Name** de um objeto [Table](table-object-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="55bc1-121">The *RelatedTable* parameter corresponds to the value of the **Name** property of a [Table](table-object-adox.md) object.</span></span>

  - <span data-ttu-id="55bc1-122">*RelatedColumn*</span><span class="sxs-lookup"><span data-stu-id="55bc1-122">*RelatedColumn*</span></span>

  - <span data-ttu-id="55bc1-p104">Opcional. Um valor **String** que especifica o nome da coluna relacionada para uma chave estrangeira. O parâmetro RelatedColumn corresponde ao valor da propriedade **Name** de um objeto **Column**.</span><span class="sxs-lookup"><span data-stu-id="55bc1-p104">Optional. A **String** value that specifies the name of the related column for a foreign key. The RelatedColumn parameter corresponds to the value of the **Name** property of a **Column** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="55bc1-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="55bc1-126">Remarks</span></span>

<span data-ttu-id="55bc1-127">O parâmetro *Columns* pode levar o nome de uma coluna ou uma matriz de nomes de coluna.</span><span class="sxs-lookup"><span data-stu-id="55bc1-127">The *Columns* parameter can take either the name of a column or an array of column names.</span></span>

