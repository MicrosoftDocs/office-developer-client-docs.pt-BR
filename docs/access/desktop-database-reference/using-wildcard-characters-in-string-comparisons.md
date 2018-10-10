---
title: Utilizando caracteres curinga em comparações de sequência
TOCTitle: Using Wildcard Characters in String Comparisons
ms:assetid: 37dda2b8-c710-4f73-bb2a-76a1348c42fe
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192499(v=office.15)
ms:contentKeyID: 48544205
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 73946560d06d12c9bdb72b41ce0f560ad9df3e65
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462956"
---
# <a name="using-wildcard-characters-in-string-comparisons"></a>Utilizando caracteres curinga em comparações de sequência


**Aplica-se a**: Access 2013 | Office 2013

A correspondência de padrões internos fornece uma ferramenta versátil para fazer comparações de sequência. A tabela a seguir mostra os caracteres curinga que você pode usar com o operador **Like** e o número de dígitos ou sequências correspondentes.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Caractere (s) em <em>pattern</em></p></th>
<th><p>Correspondências em <em>expression</em></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>? ou _ (sublinhado)</p></td>
<td><p>Qualquer caractere simples</p></td>
</tr>
<tr class="even">
<td><p>*ou %</p></td>
<td><p>Zero ou mais caracteres</p></td>
</tr>
<tr class="odd">
<td><p>#</p></td>
<td><p>Qualquer dígito único (0 – 9)</p></td>
</tr>
<tr class="even">
<td><p>[<em>charlist</em>]</p></td>
<td><p>Qualquer caractere único em <em>charlist</em></p></td>
</tr>
<tr class="odd">
<td><p>[!<em>charlist</em>]</p></td>
<td><p>Qualquer caractere único não em <em>charlist</em></p></td>
</tr>
</tbody>
</table>


Você pode usar um grupo de um ou mais caracteres (*charlist*) entre colchetes (\[ \]) corresponder a qualquer caractere único em *charlist* e de *expressão,* pode incluir quase todos os caracteres no caractere ANSI definido, incluindo dígitos. Você pode usar os caracteres especiais colchete de abertura (\[ ), ponto de interrogação (?), sinal numérico (\#) e o asterisco (\*) para corresponder a próprios diretamente apenas se entre colchetes. Não é possível usar o colchete de fechamento ( \]) dentro de um grupo para corresponder em si, mas você pode usá-lo fora de um grupo como um caractere individual.

Além de uma lista simple de caracteres entre colchetes, *charlist* pode especificar um intervalo de caracteres usando um hífen (-) para separar superior e limites inferiores do intervalo. Por exemplo, usando \[A-Z\] em *padrão* resultará em uma coincidência se a posição do caractere correspondente na *expressão* contém qualquer uma das letras maiusculas no intervalo à Z. Você pode incluir vários intervalos entre colchetes sem delimitar os intervalos. Por exemplo, \[a-zA-Z0-9\] corresponde a qualquer caractere alfanumérico.

É importante observar que os curingas ANSI SQL (%) e (\_) só estão disponíveis com o Microsoft® Jet versão 4. x e o Microsoft OLE DB Provider for Jet. Eles serão tratados como literais se utilizados no Microsoft Access ou no DAO.

A seguir estão outras regras importantes para correspondência de padrões:

  - Um ponto de exclamação (\!) no início do *charlist* significa que uma coincidência é feita se qualquer caractere, exceto aqueles em *charlist* forem encontradas na *expressão*. Quando utilizado fora dos colchetes, o ponto de exclamação faz sua própria correspondência.

  - Você pode usar o hífen (-) no início (após um ponto de exclamação se for usado) ou no final da *charlist* para corresponder ao próprio. Em outro local, o hífen identifica um intervalo de caracteres ANSI.

  - Quando você especifica um intervalo de caracteres, os caracteres devem ser exibidos em ordem de classificação crescente (A-Z ou 0-100). \[A-Z\] é um padrão válido, mas \[Z-A\] não é.

  - A sequência de caracteres \[ \] será ignorada; ele é considerado como uma cadeia de caracteres de comprimento zero ("").

