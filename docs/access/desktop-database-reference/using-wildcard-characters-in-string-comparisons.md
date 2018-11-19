---
title: Uso de caracteres curinga em comparações de sequência
TOCTitle: Using wildcard characters in string comparisons
ms:assetid: 37dda2b8-c710-4f73-bb2a-76a1348c42fe
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192499(v=office.15)
ms:contentKeyID: 48544205
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9fb6c63d5d2db1db54d52a03fef41e44a29f42c9
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026159"
---
# <a name="using-wildcard-characters-in-string-comparisons"></a><span data-ttu-id="f541c-102">Uso de caracteres curinga em comparações de sequência</span><span class="sxs-lookup"><span data-stu-id="f541c-102">Using wildcard characters in string comparisons</span></span>

<span data-ttu-id="f541c-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="f541c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f541c-p101">A correspondência de padrões internos fornece uma ferramenta versátil para fazer comparações de sequência. A tabela a seguir mostra os caracteres curinga que você pode usar com o operador **Like** e o número de dígitos ou sequências correspondentes.</span><span class="sxs-lookup"><span data-stu-id="f541c-p101">Built-in pattern matching provides a versatile tool for making string comparisons. The following table shows the wildcard characters you can use with the **Like** operator and the number of digits or strings they match.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f541c-106">Caractere (s) em <em>pattern</em></span><span class="sxs-lookup"><span data-stu-id="f541c-106">Character(s) in <em>pattern</em></span></span></p></th>
<th><p><span data-ttu-id="f541c-107">Correspondências em <em>expression</em></span><span class="sxs-lookup"><span data-stu-id="f541c-107">Matches in <em>expression</em></span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f541c-p102">? ou _ (sublinhado)</span><span class="sxs-lookup"><span data-stu-id="f541c-p102">? or _ (underscore)</span></span></p></td>
<td><p><span data-ttu-id="f541c-110">Qualquer caractere simples</span><span class="sxs-lookup"><span data-stu-id="f541c-110">Any single character</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f541c-111">\*ou %</span><span class="sxs-lookup"><span data-stu-id="f541c-111">\* or %</span></span></p></td>
<td><p><span data-ttu-id="f541c-112">Zero ou mais caracteres</span><span class="sxs-lookup"><span data-stu-id="f541c-112">Zero or more characters</span></span></p></td>
</tr>
<tr class="odd">
<td><p>#</p></td>
<td><p><span data-ttu-id="f541c-113">Qualquer dígito único (0 – 9)</span><span class="sxs-lookup"><span data-stu-id="f541c-113">Any single digit (0 – 9)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f541c-114">[<em>charlist</em>]</span><span class="sxs-lookup"><span data-stu-id="f541c-114">[<em>charlist</em>]</span></span></p></td>
<td><p><span data-ttu-id="f541c-115">Qualquer caractere único em <em>charlist</em></span><span class="sxs-lookup"><span data-stu-id="f541c-115">Any single character in <em>charlist</em></span></span></p></td>
</tr>
<tr class="odd">
<td><p>[!<em>charlist</em>]</p></td>
<td><p><span data-ttu-id="f541c-117">Qualquer caractere único não em <em>charlist</em></span><span class="sxs-lookup"><span data-stu-id="f541c-117">Any single character not in <em>charlist</em></span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f541c-118">Você pode usar um grupo de um ou mais caracteres (*charlist*) entre colchetes (\[ \]) corresponder a qualquer caractere único em *charlist* e de *expressão,* pode incluir quase todos os caracteres no caractere ANSI definido, incluindo dígitos.</span><span class="sxs-lookup"><span data-stu-id="f541c-118">You can use a group of one or more characters (*charlist*) enclosed in brackets (\[ \]) to match any single character in *expression,* and *charlist* can include almost any characters in the ANSI character set, including digits.</span></span> <span data-ttu-id="f541c-119">Você pode usar os caracteres especiais colchete de abertura (\[ ), ponto de interrogação (?), sinal numérico (\#) e o asterisco (\*) para corresponder a próprios diretamente apenas se entre colchetes.</span><span class="sxs-lookup"><span data-stu-id="f541c-119">You can use the special characters opening bracket (\[ ), question mark (?), number sign (\#), and asterisk (\*) to match themselves directly only if enclosed in brackets.</span></span> <span data-ttu-id="f541c-120">Não é possível usar o colchete de fechamento ( \]) dentro de um grupo para corresponder em si, mas você pode usá-lo fora de um grupo como um caractere individual.</span><span class="sxs-lookup"><span data-stu-id="f541c-120">You cannot use the closing bracket ( \]) within a group to match itself, but you can use it outside a group as an individual character.</span></span>

<span data-ttu-id="f541c-121">Além de uma lista simple de caracteres entre colchetes, *charlist* pode especificar um intervalo de caracteres usando um hífen (-) para separar superior e limites inferiores do intervalo.</span><span class="sxs-lookup"><span data-stu-id="f541c-121">In addition to a simple list of characters enclosed in brackets, *charlist* can specify a range of characters by using a hyphen (-) to separate the upper and lower bounds of the range.</span></span> <span data-ttu-id="f541c-122">Por exemplo, usando \[A-Z\] em *padrão* resultará em uma coincidência se a posição do caractere correspondente na *expressão* contém qualquer uma das letras maiusculas no intervalo à Z. Você pode incluir vários intervalos entre colchetes sem delimitar os intervalos.</span><span class="sxs-lookup"><span data-stu-id="f541c-122">For example, using \[A-Z\] in *pattern* results in a match if the corresponding character position in *expression* contains any of the uppercase letters in the range A through Z. You can include multiple ranges within the brackets without delimiting the ranges.</span></span> <span data-ttu-id="f541c-123">Por exemplo, \[a-zA-Z0-9\] corresponde a qualquer caractere alfanumérico.</span><span class="sxs-lookup"><span data-stu-id="f541c-123">For example, \[a-zA-Z0-9\] matches any alphanumeric character.</span></span>

<span data-ttu-id="f541c-124">É importante observar que os curingas ANSI SQL (%) e (\_) só estão disponíveis com o Microsoft Jet versão 4. x e o Microsoft OLE DB Provider for Jet.</span><span class="sxs-lookup"><span data-stu-id="f541c-124">It is important to note that the ANSI SQL wildcards (%) and (\_) are only available with Microsoft Jet version 4.X and the Microsoft OLE DB Provider for Jet.</span></span> <span data-ttu-id="f541c-125">Eles serão tratados como literais se utilizados no Microsoft Access ou no DAO.</span><span class="sxs-lookup"><span data-stu-id="f541c-125">They will be treated as literals if used through Microsoft Access or DAO.</span></span>

<span data-ttu-id="f541c-126">A seguir estão outras regras importantes para correspondência de padrões:</span><span class="sxs-lookup"><span data-stu-id="f541c-126">Other important rules for pattern matching include the following:</span></span>

- <span data-ttu-id="f541c-127">Um ponto de exclamação (\!) no início do *charlist* significa que uma coincidência é feita se qualquer caractere, exceto aqueles em *charlist* forem encontradas na *expressão*.</span><span class="sxs-lookup"><span data-stu-id="f541c-127">An exclamation mark (\!) at the beginning of *charlist* means that a match is made if any character except those in *charlist* are found in *expression*.</span></span> <span data-ttu-id="f541c-128">Quando utilizado fora dos colchetes, o ponto de exclamação faz sua própria correspondência.</span><span class="sxs-lookup"><span data-stu-id="f541c-128">When used outside brackets, the exclamation mark matches itself.</span></span>

- <span data-ttu-id="f541c-129">Você pode usar o hífen (-) no início (após um ponto de exclamação se for usado) ou no final da *charlist* para corresponder ao próprio.</span><span class="sxs-lookup"><span data-stu-id="f541c-129">You can use the hyphen (-) either at the beginning (after an exclamation mark if one is used) or at the end of *charlist* to match itself.</span></span> <span data-ttu-id="f541c-130">Em outro local, o hífen identifica um intervalo de caracteres ANSI.</span><span class="sxs-lookup"><span data-stu-id="f541c-130">In any other location, the hyphen identifies a range of ANSI characters.</span></span>

- <span data-ttu-id="f541c-131">Quando você especifica um intervalo de caracteres, os caracteres devem ser exibidos em ordem de classificação crescente (A-Z ou 0-100).</span><span class="sxs-lookup"><span data-stu-id="f541c-131">When you specify a range of characters, the characters must appear in ascending sort order (A-Z or 0-100).</span></span> <span data-ttu-id="f541c-132">\[A-Z\] é um padrão válido, mas \[Z-A\] não é.</span><span class="sxs-lookup"><span data-stu-id="f541c-132">\[A-Z\] is a valid pattern, but \[Z-A\] is not.</span></span>

- <span data-ttu-id="f541c-133">A sequência de caracteres \[ \] será ignorada; ele é considerado como uma cadeia de caracteres de comprimento zero ("").</span><span class="sxs-lookup"><span data-stu-id="f541c-133">The character sequence \[ \] is ignored; it is considered to be a zero-length string ("").</span></span>

