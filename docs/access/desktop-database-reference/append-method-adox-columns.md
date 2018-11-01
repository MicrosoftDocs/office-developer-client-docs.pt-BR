---
title: Método Append (Colunas do ADOX)
TOCTitle: Append Method (ADOX Columns)
ms:assetid: e256a478-abc0-f15b-fc29-1b52e354144a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250152(v=office.15)
ms:contentKeyID: 48548285
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ec64241bf63719fe4f5c547d60a93f7804f181ca
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25877657"
---
# <a name="append-method-adox-columns"></a><span data-ttu-id="42148-102">Método Append (Colunas do ADOX)</span><span class="sxs-lookup"><span data-stu-id="42148-102">Append Method (ADOX Columns)</span></span>


<span data-ttu-id="42148-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="42148-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="42148-104">Adiciona um novo objeto [Column](column-object-adox.md) à coleção [Columns](columns-collection-adox.md).</span><span class="sxs-lookup"><span data-stu-id="42148-104">Adds a new [Column](column-object-adox.md) object to the [Columns](columns-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="42148-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="42148-105">Syntax</span></span>

<span data-ttu-id="42148-106">*Colunas*.</span><span class="sxs-lookup"><span data-stu-id="42148-106">*Columns*.</span></span> <span data-ttu-id="42148-107">Acrescentar*coluna* \[,*tipo* \] \[,*DefinedSize*\]</span><span class="sxs-lookup"><span data-stu-id="42148-107">Append*Column* \[,*Type*\] \[,*DefinedSize*\]</span></span>

## <a name="parameters"></a><span data-ttu-id="42148-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="42148-108">Parameters</span></span>

  - <span data-ttu-id="42148-109">*Column*</span><span class="sxs-lookup"><span data-stu-id="42148-109">*Column*</span></span>

  - <span data-ttu-id="42148-110">O objeto **Column** a ser anexado ou o nome da coluna a ser criada e anexada.</span><span class="sxs-lookup"><span data-stu-id="42148-110">The **Column** object to append or the name of the column to create and append.</span></span>

  - <span data-ttu-id="42148-111">*Type*</span><span class="sxs-lookup"><span data-stu-id="42148-111">*Type*</span></span>

  - <span data-ttu-id="42148-112">Opcional.</span><span class="sxs-lookup"><span data-stu-id="42148-112">Optional.</span></span> <span data-ttu-id="42148-113">Um valor **Long** que especifica o tipo de dados da coluna.</span><span class="sxs-lookup"><span data-stu-id="42148-113">A **Long** value that specifies the data type of the column.</span></span> <span data-ttu-id="42148-114">O parâmetro *Type* corresponde à propriedade [Type](https://msdn.microsoft.com/library/jj249169\(v=office.15\)) de um objeto **Column** .</span><span class="sxs-lookup"><span data-stu-id="42148-114">The *Type* parameter corresponds to the [Type](https://msdn.microsoft.com/library/jj249169\(v=office.15\)) property of a **Column** object.</span></span>

  - <span data-ttu-id="42148-115">*DefinedSize*</span><span class="sxs-lookup"><span data-stu-id="42148-115">*DefinedSize*</span></span>

  - <span data-ttu-id="42148-116">Opcional.</span><span class="sxs-lookup"><span data-stu-id="42148-116">Optional.</span></span> <span data-ttu-id="42148-117">Um valor **Long** que especifica o tamanho da coluna.</span><span class="sxs-lookup"><span data-stu-id="42148-117">A **Long** value that specifies the size of the column.</span></span> <span data-ttu-id="42148-118">O parâmetro *DefinedSize* corresponde à propriedade [DefinedSize](definedsize-property-adox.md) de um objeto **Column** .</span><span class="sxs-lookup"><span data-stu-id="42148-118">The *DefinedSize* parameter corresponds to the [DefinedSize](definedsize-property-adox.md) property of a **Column** object.</span></span>


> [!NOTE]
> <span data-ttu-id="42148-119">[!OBSERVAçãO] Ocorrerá um erro ao anexar uma **Coluna** à coleção **Columns** de um [Índice](index-object-adox.md), se a **Coluna** não existir em uma [Tabela](table-object-adox.md) que já esteja anexada à coleção [Tables](tables-collection-adox.md).</span><span class="sxs-lookup"><span data-stu-id="42148-119">An error will occur when appending a **Column** to the **Columns** collection of an [Index](index-object-adox.md) if the **Column** does not exist in a [Table](table-object-adox.md) that is already appended to the [Tables](tables-collection-adox.md) collection.</span></span>


