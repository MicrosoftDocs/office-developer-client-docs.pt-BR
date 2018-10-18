---
title: Método CompareBookmarks (ADO)
TOCTitle: CompareBookmarks Method (ADO)
ms:assetid: 826cb3c7-2f5c-284f-421d-6b7b07f14dec
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249564(v=office.15)
ms:contentKeyID: 48545977
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9fc4cf3540d22d3981bb13a7af3251dd625c2c99
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25606245"
---
# <a name="comparebookmarks-method-ado"></a><span data-ttu-id="f61ea-102">Método CompareBookmarks (ADO)</span><span class="sxs-lookup"><span data-stu-id="f61ea-102">CompareBookmarks Method (ADO)</span></span>


<span data-ttu-id="f61ea-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="f61ea-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="f61ea-104">Compara dois indicadores e retorna uma indicação de seus valores relativos.</span><span class="sxs-lookup"><span data-stu-id="f61ea-104">Compares two bookmarks and returns an indication of their relative values.</span></span>

## <a name="syntax"></a><span data-ttu-id="f61ea-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f61ea-105">Syntax</span></span>

<span data-ttu-id="f61ea-106">*resultado* = *recordset*. CompareBookmarks (*Bookmark1*, *Bookmark2*)</span><span class="sxs-lookup"><span data-stu-id="f61ea-106">*result* = *recordset*.CompareBookmarks(*Bookmark1*, *Bookmark2*)</span></span>

<span data-ttu-id="f61ea-107"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="f61ea-107"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="f61ea-108">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="f61ea-108">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="f61ea-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="f61ea-109">Return value</span></span>
>>>>>>> <span data-ttu-id="f61ea-110">mestre</span><span class="sxs-lookup"><span data-stu-id="f61ea-110">master</span></span>

<span data-ttu-id="f61ea-111">Retorna um valor [CompareEnum](compareenum.md) que indica a posição de linha relativa de dois registros representados por seus indicadores.</span><span class="sxs-lookup"><span data-stu-id="f61ea-111">Returns a [CompareEnum](compareenum.md) value that indicates the relative row position of two records represented by their bookmarks.</span></span>

## <a name="parameters"></a><span data-ttu-id="f61ea-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f61ea-112">Parameters</span></span>

  - <span data-ttu-id="f61ea-113">*Bookmark1*</span><span class="sxs-lookup"><span data-stu-id="f61ea-113">*Bookmark1*</span></span>

  - <span data-ttu-id="f61ea-114">O indicador da primeira linha.</span><span class="sxs-lookup"><span data-stu-id="f61ea-114">The bookmark of the first row.</span></span>

  - <span data-ttu-id="f61ea-115">*Bookmark2*</span><span class="sxs-lookup"><span data-stu-id="f61ea-115">*Bookmark2*</span></span>

  - <span data-ttu-id="f61ea-116">O indicador da segunda linha.</span><span class="sxs-lookup"><span data-stu-id="f61ea-116">The bookmark of the second row.</span></span>

## <a name="remarks"></a><span data-ttu-id="f61ea-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="f61ea-117">Remarks</span></span>

<span data-ttu-id="f61ea-p101">Os indicadores devem ser aplicados ao mesmo objeto [Recordset](recordset-object-ado.md), ou a um objeto **Recordset** e seu [clone](clone-method-ado.md). Não é possível comparar com segurança indicadores de objetos **Recordset** diferentes, mesmo se eles foram criados a partir da mesma fonte ou comando. Também não é possível comparar indicadores para um objeto **Recordset** cujo provedor base não suporte comparações.</span><span class="sxs-lookup"><span data-stu-id="f61ea-p101">The bookmarks must apply to the same [Recordset](recordset-object-ado.md) object, or a **Recordset** object and its [clone](clone-method-ado.md). You cannot reliably compare bookmarks from different **Recordset** objects, even if they were created from the same source or command. Nor can you compare bookmarks for a **Recordset** object whose underlying provider does not support comparisons.</span></span>

<span data-ttu-id="f61ea-p102">Um indicador identifica exclusivamente uma linha em um objeto **Recordset**. Utilize a propriedade [Bookmark](bookmark-property-ado.md) da linha atual para obter seu indicador.</span><span class="sxs-lookup"><span data-stu-id="f61ea-p102">A bookmark uniquely identifies a row in a **Recordset** object. Use the current row's [Bookmark](bookmark-property-ado.md) property to obtain its bookmark.</span></span>

<span data-ttu-id="f61ea-123">Como o tipo de dados de um indicador é específico do provedor, o ADO o expõe como uma Variant.</span><span class="sxs-lookup"><span data-stu-id="f61ea-123">Because the data type of a bookmark is provider specific, ADO exposes it as a Variant.</span></span> <span data-ttu-id="f61ea-124">Por exemplo, os indicadores do SQL Server são do tipo DBTYPE\_R8 (Double).</span><span class="sxs-lookup"><span data-stu-id="f61ea-124">For example, SQL Server bookmarks are of type DBTYPE\_R8 (Double).</span></span> <span data-ttu-id="f61ea-125">O ADO exporá esse tipo como uma Variant com um subtipo igual a Double.</span><span class="sxs-lookup"><span data-stu-id="f61ea-125">ADO would expose this type as a Variant with a subtype of Double.</span></span>

<span data-ttu-id="f61ea-p104">Ao comparar indicadores, o ADO não tenta nenhum tipo de imposição. Os valores são simplesmente passados para o provedor onde a comparação ocorre. Se os indicadores passados para o método **CompareBookmarks** forem armazenados em variáveis de tipos diferentes, ele pode gerar o erro de tipos incompatíveis "Os argumentos são do tipo errado, estão fora do intervalo aceitável ou estão em conflito entre si."</span><span class="sxs-lookup"><span data-stu-id="f61ea-p104">When comparing bookmarks, ADO does not attempt any type of coercion. The values are simply passed to the provider where the compare occurs. If bookmarks passed to the **CompareBookmarks** method are stored in variables of differing types, it can generate the type mismatch error, "Arguments are of the wrong type, are out of the acceptable range, or are in conflict with each other."</span></span>

<span data-ttu-id="f61ea-129">Um indicador que não seja válido ou esteja formado incorretamente causará um erro.</span><span class="sxs-lookup"><span data-stu-id="f61ea-129">A bookmark that is not valid or incorrectly formed will cause an error.</span></span>

