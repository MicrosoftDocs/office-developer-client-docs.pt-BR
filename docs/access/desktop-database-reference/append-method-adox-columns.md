---
title: Método Append (Colunas do ADOX)
TOCTitle: Append Method (ADOX Columns)
ms:assetid: e256a478-abc0-f15b-fc29-1b52e354144a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250152(v=office.15)
ms:contentKeyID: 48548285
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1f64f3b04df989348173ad2fc975dcefbd1114b2
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462431"
---
# <a name="append-method-adox-columns"></a><span data-ttu-id="391a2-102">Método Append (Colunas do ADOX)</span><span class="sxs-lookup"><span data-stu-id="391a2-102">Append Method (ADOX Columns)</span></span>


<span data-ttu-id="391a2-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="391a2-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="391a2-104">Adiciona um novo objeto [Column](column-object-adox.md) à coleção [Columns](columns-collection-adox.md).</span><span class="sxs-lookup"><span data-stu-id="391a2-104">Adds a new [Column](column-object-adox.md) object to the [Columns](columns-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="391a2-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="391a2-105">Syntax</span></span>

<span data-ttu-id="391a2-106">*Colunas*.</span><span class="sxs-lookup"><span data-stu-id="391a2-106">*Columns*.</span></span> <span data-ttu-id="391a2-107">Acrescentar*coluna* \[,*tipo* \] \[,*DefinedSize*\]</span><span class="sxs-lookup"><span data-stu-id="391a2-107">Append*Column* \[,*Type*\] \[,*DefinedSize*\]</span></span>

## <a name="parameters"></a><span data-ttu-id="391a2-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="391a2-108">Parameters</span></span>

  - <span data-ttu-id="391a2-109">*Column*</span><span class="sxs-lookup"><span data-stu-id="391a2-109">*Column*</span></span>

  - <span data-ttu-id="391a2-110">O objeto **Column** a ser anexado ou o nome da coluna a ser criada e anexada.</span><span class="sxs-lookup"><span data-stu-id="391a2-110">The **Column** object to append or the name of the column to create and append.</span></span>

  - <span data-ttu-id="391a2-111">*Type*</span><span class="sxs-lookup"><span data-stu-id="391a2-111">*Type*</span></span>

  - <span data-ttu-id="391a2-112">Opcional.</span><span class="sxs-lookup"><span data-stu-id="391a2-112">Optional.</span></span> <span data-ttu-id="391a2-113">Um valor **Long** que especifica o tipo de dados da coluna.</span><span class="sxs-lookup"><span data-stu-id="391a2-113">A **Long** value that specifies the data type of the column.</span></span> <span data-ttu-id="391a2-114">O parâmetro *Type* corresponde à propriedade [Type](https://msdn.microsoft.com/library/jj249169\(v=office.15\)) de um objeto **Column** .</span><span class="sxs-lookup"><span data-stu-id="391a2-114">The *Type* parameter corresponds to the [Type](https://msdn.microsoft.com/library/jj249169\(v=office.15\)) property of a **Column** object.</span></span>

  - <span data-ttu-id="391a2-115">*DefinedSize*</span><span class="sxs-lookup"><span data-stu-id="391a2-115">*DefinedSize*</span></span>

  - <span data-ttu-id="391a2-116">Opcional.</span><span class="sxs-lookup"><span data-stu-id="391a2-116">Optional.</span></span> <span data-ttu-id="391a2-117">Um valor **Long** que especifica o tamanho da coluna.</span><span class="sxs-lookup"><span data-stu-id="391a2-117">A **Long** value that specifies the size of the column.</span></span> <span data-ttu-id="391a2-118">O parâmetro *DefinedSize* corresponde à propriedade [DefinedSize](definedsize-property-adox.md) de um objeto **Column** .</span><span class="sxs-lookup"><span data-stu-id="391a2-118">The *DefinedSize* parameter corresponds to the [DefinedSize](definedsize-property-adox.md) property of a **Column** object.</span></span>


> [!NOTE]
> <P><span data-ttu-id="391a2-119">[!OBSERVAçãO] Ocorrerá um erro ao anexar uma <STRONG>Coluna</STRONG> à coleção <STRONG>Columns</STRONG> de um <A href="index-object-adox.md">Índice</A>, se a <STRONG>Coluna</STRONG> não existir em uma <A href="table-object-adox.md">Tabela</A> que já esteja anexada à coleção <A href="tables-collection-adox.md">Tables</A>.</span><span class="sxs-lookup"><span data-stu-id="391a2-119">An error will occur when appending a <STRONG>Column</STRONG> to the <STRONG>Columns</STRONG> collection of an <A href="index-object-adox.md">Index</A> if the <STRONG>Column</STRONG> does not exist in a <A href="table-object-adox.md">Table</A> that is already appended to the <A href="tables-collection-adox.md">Tables</A> collection.</span></span></P>


