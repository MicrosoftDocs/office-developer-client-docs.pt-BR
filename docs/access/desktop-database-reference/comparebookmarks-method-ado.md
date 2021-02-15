---
title: Método CompareBookmarks (ADO)
TOCTitle: CompareBookmarks method (ADO)
ms:assetid: 826cb3c7-2f5c-284f-421d-6b7b07f14dec
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249564(v=office.15)
ms:contentKeyID: 48545977
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 460a77284141daad1834699c4dc1775be05c5c26
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296091"
---
# <a name="comparebookmarks-method-ado"></a><span data-ttu-id="27453-102">Método CompareBookmarks (ADO)</span><span class="sxs-lookup"><span data-stu-id="27453-102">CompareBookmarks method (ADO)</span></span>

<span data-ttu-id="27453-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="27453-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="27453-104">Compara dois indicadores e retorna uma indicação de seus valores relativos.</span><span class="sxs-lookup"><span data-stu-id="27453-104">Compares two bookmarks and returns an indication of their relative values.</span></span>

## <a name="syntax"></a><span data-ttu-id="27453-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="27453-105">Syntax</span></span>

<span data-ttu-id="27453-106">*result*  =  *recordset*. CompareBookmarks(*Bookmark1*, *Bookmark2*)</span><span class="sxs-lookup"><span data-stu-id="27453-106">*result* = *recordset*.CompareBookmarks(*Bookmark1*, *Bookmark2*)</span></span>

## <a name="return-value"></a><span data-ttu-id="27453-107">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="27453-107">Return value</span></span>

<span data-ttu-id="27453-108">Retorna um valor [CompareEnum](compareenum.md) que indica a posição de linha relativa de dois registros representados por seus indicadores.</span><span class="sxs-lookup"><span data-stu-id="27453-108">Returns a [CompareEnum](compareenum.md) value that indicates the relative row position of two records represented by their bookmarks.</span></span>

## <a name="parameters"></a><span data-ttu-id="27453-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="27453-109">Parameters</span></span>

|<span data-ttu-id="27453-110">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="27453-110">Parameter</span></span>|<span data-ttu-id="27453-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="27453-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="27453-112">*Bookmark1*</span><span class="sxs-lookup"><span data-stu-id="27453-112">*Bookmark1*</span></span> |<span data-ttu-id="27453-113">O indicador da primeira linha.</span><span class="sxs-lookup"><span data-stu-id="27453-113">The bookmark of the first row.</span></span>|
|<span data-ttu-id="27453-114">*Bookmark2*</span><span class="sxs-lookup"><span data-stu-id="27453-114">*Bookmark2*</span></span> |<span data-ttu-id="27453-115">O indicador da segunda linha.</span><span class="sxs-lookup"><span data-stu-id="27453-115">The bookmark of the second row.</span></span>|

## <a name="remarks"></a><span data-ttu-id="27453-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="27453-116">Remarks</span></span>

<span data-ttu-id="27453-p101">Os indicadores devem ser aplicados ao mesmo objeto [Recordset](recordset-object-ado.md), ou a um objeto **Recordset** e seu [clone](clone-method-ado.md). Não é possível comparar com segurança indicadores de objetos **Recordset** diferentes, mesmo se eles foram criados a partir da mesma fonte ou comando. Também não é possível comparar indicadores para um objeto **Recordset** cujo provedor base não suporte comparações.</span><span class="sxs-lookup"><span data-stu-id="27453-p101">The bookmarks must apply to the same [Recordset](recordset-object-ado.md) object, or a **Recordset** object and its [clone](clone-method-ado.md). You cannot reliably compare bookmarks from different **Recordset** objects, even if they were created from the same source or command. Nor can you compare bookmarks for a **Recordset** object whose underlying provider does not support comparisons.</span></span>

<span data-ttu-id="27453-p102">Um indicador identifica exclusivamente uma linha em um objeto **Recordset**. Utilize a propriedade [Bookmark](bookmark-property-ado.md) da linha atual para obter seu indicador.</span><span class="sxs-lookup"><span data-stu-id="27453-p102">A bookmark uniquely identifies a row in a **Recordset** object. Use the current row's [Bookmark](bookmark-property-ado.md) property to obtain its bookmark.</span></span>

<span data-ttu-id="27453-122">Como o tipo de dados de um indicador é específico do provedor, o ADO o expõe como uma Variant.</span><span class="sxs-lookup"><span data-stu-id="27453-122">Because the data type of a bookmark is provider specific, ADO exposes it as a Variant.</span></span> <span data-ttu-id="27453-123">Por exemplo, os indicadores do SQL Server são do tipo DBTYPE \_ R8 (Double).</span><span class="sxs-lookup"><span data-stu-id="27453-123">For example, SQL Server bookmarks are of type DBTYPE\_R8 (Double).</span></span> <span data-ttu-id="27453-124">O ADO exporá esse tipo como uma Variant com um subtipo igual a Double.</span><span class="sxs-lookup"><span data-stu-id="27453-124">ADO would expose this type as a Variant with a subtype of Double.</span></span>

<span data-ttu-id="27453-p104">Ao comparar indicadores, o ADO não tenta nenhum tipo de imposição. Os valores são simplesmente passados para o provedor onde a comparação ocorre. Se os indicadores passados para o método **CompareBookmarks** forem armazenados em variáveis de tipos diferentes, ele pode gerar o erro de tipos incompatíveis "Os argumentos são do tipo errado, estão fora do intervalo aceitável ou estão em conflito entre si."</span><span class="sxs-lookup"><span data-stu-id="27453-p104">When comparing bookmarks, ADO does not attempt any type of coercion. The values are simply passed to the provider where the compare occurs. If bookmarks passed to the **CompareBookmarks** method are stored in variables of differing types, it can generate the type mismatch error, "Arguments are of the wrong type, are out of the acceptable range, or are in conflict with each other."</span></span>

<span data-ttu-id="27453-128">Um indicador que não seja válido ou esteja formado incorretamente causará um erro.</span><span class="sxs-lookup"><span data-stu-id="27453-128">A bookmark that is not valid or incorrectly formed will cause an error.</span></span>

