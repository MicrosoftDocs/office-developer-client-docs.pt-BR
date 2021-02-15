---
title: Uso de caracteres curinga em comparações de sequência
TOCTitle: Using wildcard characters in string comparisons
ms:assetid: 37dda2b8-c710-4f73-bb2a-76a1348c42fe
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192499(v=office.15)
ms:contentKeyID: 48544205
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e6a013865b9615701b1d99678fc2392e0a896c54
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32305933"
---
# <a name="using-wildcard-characters-in-string-comparisons"></a><span data-ttu-id="045a3-102">Uso de caracteres curinga em comparações de sequência</span><span class="sxs-lookup"><span data-stu-id="045a3-102">Using wildcard characters in string comparisons</span></span>

<span data-ttu-id="045a3-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="045a3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="045a3-p101">A correspondência de padrões internos fornece uma ferramenta versátil para fazer comparações de sequência. A tabela a seguir mostra os caracteres curinga que você pode usar com o operador **Like** e o número de dígitos ou sequências correspondentes.</span><span class="sxs-lookup"><span data-stu-id="045a3-p101">Built-in pattern matching provides a versatile tool for making string comparisons. The following table shows the wildcard characters you can use with the **Like** operator and the number of digits or strings they match.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="045a3-106">Caractere(s) em <em>pattern</em></span><span class="sxs-lookup"><span data-stu-id="045a3-106">Character(s) in <em>pattern</em></span></span></p></th>
<th><p><span data-ttu-id="045a3-107">Correspondências em <em>expression</em></span><span class="sxs-lookup"><span data-stu-id="045a3-107">Matches in <em>expression</em></span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="045a3-p102">? ou _ (sublinhado)</span><span class="sxs-lookup"><span data-stu-id="045a3-p102">? or _ (underscore)</span></span></p></td>
<td><p><span data-ttu-id="045a3-110">Qualquer caractere simples</span><span class="sxs-lookup"><span data-stu-id="045a3-110">Any single character</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="045a3-111">\* ou %</span><span class="sxs-lookup"><span data-stu-id="045a3-111">\* or %</span></span></p></td>
<td><p><span data-ttu-id="045a3-112">Zero ou mais caracteres</span><span class="sxs-lookup"><span data-stu-id="045a3-112">Zero or more characters</span></span></p></td>
</tr>
<tr class="odd">
<td><p>#</p></td>
<td><p><span data-ttu-id="045a3-113">Qualquer dígito único (0 – 9)</span><span class="sxs-lookup"><span data-stu-id="045a3-113">Any single digit (0 – 9)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="045a3-114">[<em>charlist</em>]</span><span class="sxs-lookup"><span data-stu-id="045a3-114">[<em>charlist</em>]</span></span></p></td>
<td><p><span data-ttu-id="045a3-115">Qualquer caractere único em <em>charlist</em></span><span class="sxs-lookup"><span data-stu-id="045a3-115">Any single character in <em>charlist</em></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="045a3-116">[! <em>charlist</em>]</span><span class="sxs-lookup"><span data-stu-id="045a3-116">[!<em>charlist</em>]</span></span></p></td>
<td><p><span data-ttu-id="045a3-117">Qualquer caractere único não em <em>charlist</em></span><span class="sxs-lookup"><span data-stu-id="045a3-117">Any single character not in <em>charlist</em></span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="045a3-118">Você pode usar um grupo de um ou mais caracteres (*charlist*) entre colchetes ( ) para corresponder a qualquer caractere único na expressão, e charlist pode incluir quase todos os caracteres no conjunto de \[ \] caracteres  ANSI, incluindo dígitos. </span><span class="sxs-lookup"><span data-stu-id="045a3-118">You can use a group of one or more characters (*charlist*) enclosed in brackets (\[ \]) to match any single character in *expression,* and *charlist* can include almost any characters in the ANSI character set, including digits.</span></span> <span data-ttu-id="045a3-119">Você pode usar o colchete de abertura de caracteres especiais ( ), ponto de interrogação (?), sinal de número ( ) e asterisco ( ) para corresponder a si mesmos diretamente somente se estiver entre \[ \# \* colchetes.</span><span class="sxs-lookup"><span data-stu-id="045a3-119">You can use the special characters opening bracket (\[ ), question mark (?), number sign (\#), and asterisk (\*) to match themselves directly only if enclosed in brackets.</span></span> <span data-ttu-id="045a3-120">Você não pode usar o colchete de fechamento ( ) dentro de um grupo para se corresponder a si mesmo, mas você pode usá-lo fora de um \] grupo como um caractere individual.</span><span class="sxs-lookup"><span data-stu-id="045a3-120">You cannot use the closing bracket ( \]) within a group to match itself, but you can use it outside a group as an individual character.</span></span>

<span data-ttu-id="045a3-121">Além de uma simples lista de caracteres entre colchetes, *charlist* pode especificar um intervalo de caracteres utilizando um hífen (-) para separar limites superiores e inferiores do intervalo.</span><span class="sxs-lookup"><span data-stu-id="045a3-121">In addition to a simple list of characters enclosed in brackets, *charlist* can specify a range of characters by using a hyphen (-) to separate the upper and lower bounds of the range.</span></span> <span data-ttu-id="045a3-122">Por exemplo, usar A-Z no padrão resulta em uma correspondência se a posição de caractere correspondente na expressão contiver qualquer uma das letras maiúsculas no intervalo \[ \] de A a Z.   Você pode incluir vários intervalos entre colchetes sem delimitar os intervalos.</span><span class="sxs-lookup"><span data-stu-id="045a3-122">For example, using \[A-Z\] in *pattern* results in a match if the corresponding character position in *expression* contains any of the uppercase letters in the range A through Z. You can include multiple ranges within the brackets without delimiting the ranges.</span></span> <span data-ttu-id="045a3-123">Por exemplo, \[ a-zA-Z0-9 corresponde a \] qualquer caractere alfanumérico.</span><span class="sxs-lookup"><span data-stu-id="045a3-123">For example, \[a-zA-Z0-9\] matches any alphanumeric character.</span></span>

<span data-ttu-id="045a3-124">É importante observar que os caracteres curinga do ANSI SQL (%) e ( ) só estão disponíveis com o \_ Microsoft Jet versão 4.X e o Microsoft OLE DB Provider for Jet.</span><span class="sxs-lookup"><span data-stu-id="045a3-124">It is important to note that the ANSI SQL wildcards (%) and (\_) are only available with Microsoft Jet version 4.X and the Microsoft OLE DB Provider for Jet.</span></span> <span data-ttu-id="045a3-125">Eles serão tratados como literais se utilizados no Microsoft Access ou no DAO.</span><span class="sxs-lookup"><span data-stu-id="045a3-125">They will be treated as literals if used through Microsoft Access or DAO.</span></span>

<span data-ttu-id="045a3-126">A seguir estão outras regras importantes para correspondência de padrões:</span><span class="sxs-lookup"><span data-stu-id="045a3-126">Other important rules for pattern matching include the following:</span></span>

- <span data-ttu-id="045a3-127">Um ponto de exclamação ( ) no início da lista de caracteres significa que uma combinação será feita se qualquer caractere, exceto aqueles na lista de caracteres, for \! encontrado na *expressão*.  </span><span class="sxs-lookup"><span data-stu-id="045a3-127">An exclamation mark (\!) at the beginning of *charlist* means that a match is made if any character except those in *charlist* are found in *expression*.</span></span> <span data-ttu-id="045a3-128">Quando utilizado fora dos colchetes, o ponto de exclamação faz sua própria correspondência.</span><span class="sxs-lookup"><span data-stu-id="045a3-128">When used outside brackets, the exclamation mark matches itself.</span></span>

- <span data-ttu-id="045a3-p107">Você pode usar o hífen (-) no início (após um ponto de exclamação, se utilizado) ou no final da *charlist* para sua própria correspondência. Em outro local, o hífen identifica um intervalo de caracteres ANSI.</span><span class="sxs-lookup"><span data-stu-id="045a3-p107">You can use the hyphen (-) either at the beginning (after an exclamation mark if one is used) or at the end of *charlist* to match itself. In any other location, the hyphen identifies a range of ANSI characters.</span></span>

- <span data-ttu-id="045a3-131">Quando você especifica um intervalo de caracteres, os caracteres devem ser exibidos em ordem de classificação crescente (A-Z ou 0-100).</span><span class="sxs-lookup"><span data-stu-id="045a3-131">When you specify a range of characters, the characters must appear in ascending sort order (A-Z or 0-100).</span></span> <span data-ttu-id="045a3-132">\[A-Z \] é um padrão válido, mas \[ Z-A \] não é.</span><span class="sxs-lookup"><span data-stu-id="045a3-132">\[A-Z\] is a valid pattern, but \[Z-A\] is not.</span></span>

- <span data-ttu-id="045a3-133">A sequência de caracteres é ignorada; ela é considerada \[ \] uma cadeia de caracteres de comprimento zero ("").</span><span class="sxs-lookup"><span data-stu-id="045a3-133">The character sequence \[ \] is ignored; it is considered to be a zero-length string ("").</span></span>

