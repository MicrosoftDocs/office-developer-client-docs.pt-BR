---
title: Propriedade Sort (ADO)
TOCTitle: Sort property (ADO)
ms:assetid: f2a39b7f-8b96-cd1a-8248-71f8b867454a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250230(v=office.15)
ms:contentKeyID: 48548652
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ebd515d2812ce453711c2b6519b1875250911d1a
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25886603"
---
# <a name="sort-property-ado"></a><span data-ttu-id="95760-102">Propriedade Sort (ADO)</span><span class="sxs-lookup"><span data-stu-id="95760-102">Sort property (ADO)</span></span>


<span data-ttu-id="95760-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="95760-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="95760-104">Indica um ou mais nomes de campo nos quais o [Recordset](recordset-object-ado.md) é classificado e se cada campo é classificado na ordem crescente ou decrescente.</span><span class="sxs-lookup"><span data-stu-id="95760-104">Indicates one or more field names on which the [Recordset](recordset-object-ado.md) is sorted, and whether each field is sorted in ascending or descending order.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="95760-105">Configurações e valores de retorno</span><span class="sxs-lookup"><span data-stu-id="95760-105">Settings and return values</span></span>

<span data-ttu-id="95760-p101">Define ou retorna um valor **String** que indica os nomes dos campos do **Recordset** no qual classificá-los. Cada nome é separado por uma vírgula e é, opcionalmente, seguido por um espaço em branco e pela palavra-chave, **ASC**, que classifica o campo na ordem crescente ou **DESC**, que classifica o campo na ordem decrescente. Por padrão, se nenhuma palavra-chave for especificada, o campo será classificado na ordem crescente.</span><span class="sxs-lookup"><span data-stu-id="95760-p101">Sets or returns a **String** value that indicates the field names in the **Recordset** on which to sort. Each name is separated by a comma, and is optionally followed by a blank and the keyword, **ASC**, which sorts the field in ascending order, or **DESC**, which sorts the field in descending order. By default, if no keyword is specified, the field is sorted in ascending order.</span></span>

## <a name="remarks"></a><span data-ttu-id="95760-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="95760-109">Remarks</span></span>

<span data-ttu-id="95760-p102">Essa propriedade exige que a propriedade [CursorLocation](cursorlocation-property-ado.md) seja definida como **adUseClient**. Se ainda não existir um índice, será criado um temporário para cada campo especificado na propriedade **Sort**.</span><span class="sxs-lookup"><span data-stu-id="95760-p102">This property requires the [CursorLocation](cursorlocation-property-ado.md) property to be set to **adUseClient**. A temporary index will be created for each field specified in the **Sort** property if an index does not already exist.</span></span>

<span data-ttu-id="95760-112">A operação de classificação é eficiente, pois os dados não são reorganizados fisicamente, mas simplesmente acessados na ordem especificada pelo índice.</span><span class="sxs-lookup"><span data-stu-id="95760-112">The sort operation is efficient because data is not physically rearranged, but is simply accessed in the order specified by the index.</span></span>

<span data-ttu-id="95760-p103">A definição da propriedade **Sort** em uma sequência de caracteres vazia redefinirá as linhas para sua ordem original e excluirá os índices temporários. Os índices existentes não serão excluídos.</span><span class="sxs-lookup"><span data-stu-id="95760-p103">Setting the **Sort** property to an empty string will reset the rows to their original order and delete temporary indexes. Existing indexes will not be deleted.</span></span>

<span data-ttu-id="95760-115">Suponha que um **Recordset** contém três campos chamado *"MiddleInitial"*, *firstName*e *lastName*.</span><span class="sxs-lookup"><span data-stu-id="95760-115">Suppose a **Recordset** contains three fields named *firstName*, *middleInitial*, and *lastName*.</span></span> <span data-ttu-id="95760-116">Definir a propriedade **Sort** à cadeia de caracteres, "Sobrenome DESC, firstName ASC", que será ordenar o **conjunto de registros** por sobrenome em ordem decrescente e, em seguida, por nome em ordem crescente.</span><span class="sxs-lookup"><span data-stu-id="95760-116">Set the **Sort** property to the string, "lastName DESC, firstName ASC", which will order the **Recordset** by last name in descending order, then by first name in ascending order.</span></span> <span data-ttu-id="95760-117">A inicial do segundo nome será ignorada.</span><span class="sxs-lookup"><span data-stu-id="95760-117">The middle initial is ignored.</span></span>

<span data-ttu-id="95760-p105">Nenhum campo poderá ser nomeado como "ASC" ou "DESC", pois esses nomes entrariam em conflito com as palavras-chave **ASC** e **DESC**. Forneça um alias ao campo com um nome conflitante utilizando a palavra-chave **AS** na consulta que retornar o **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="95760-p105">No field can be named "ASC" or "DESC" because those names conflict with the keywords **ASC** and **DESC**. Give a field with a conflicting name an alias by using the **AS** keyword in the query that returns the **Recordset**.</span></span>

