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
# <a name="using-wildcard-characters-in-string-comparisons"></a>Uso de caracteres curinga em comparações de sequência

**Aplica-se ao:** Access 2013, Office 2013

A correspondência de padrões internos fornece uma ferramenta versátil para fazer comparações de sequência. A tabela a seguir mostra os caracteres curinga que você pode usar com o operador **Like** e o número de dígitos ou sequências correspondentes.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Caractere(s) em <em>pattern</em></p></th>
<th><p>Correspondências em <em>expression</em></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>? ou _ (sublinhado)</p></td>
<td><p>Qualquer caractere simples</p></td>
</tr>
<tr class="even">
<td><p>*ou</p></td>
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
<td><p>[! <em>charlist</em>]</p></td>
<td><p>Qualquer caractere único não em <em>charlist</em></p></td>
</tr>
</tbody>
</table>


Você pode usar um grupo de um ou mais caracteres (*charlist*) entre\[ \]colchetes () para corresponder a qualquer caractere único em *Expression,* e *charlist* pode incluir quase todos os caracteres no conjunto de caracteres ANSI, incluindo dígito. Você pode usar o colchete de abertura de caracteres\[ especiais (), o ponto de interrogação (?\#), o sinal de\*número () e o asterisco () para fazer a correspondência deles diretamente apenas se estiverem entre colchetes. Não é possível usar o colchete de \]fechamento () dentro de um grupo para corresponder a si mesmo, mas você pode usá-lo fora de um grupo como um caractere individual.

Além de uma simples lista de caracteres entre colchetes, *charlist* pode especificar um intervalo de caracteres utilizando um hífen (-) para separar limites superiores e inferiores do intervalo. Por exemplo, o \[uso de A\] -Z no *padrão* resulta em uma correspondência se a posição do caractere correspondente na *expressão* contiver qualquer uma das letras maiúsculas no intervalo de a a Z. Você pode incluir vários intervalos dentro dos colchetes sem delimitar os intervalos. Por exemplo, \[a-zA-Z0-9\] corresponde a qualquer caractere alfanumérico.

É importante observar que os curingas ANSI SQL (%) e (\_) só estão disponíveis com o Microsoft Jet versão 4. X e o Microsoft OLE DB Provider for Jet. Eles serão tratados como literais se utilizados no Microsoft Access ou no DAO.

A seguir estão outras regras importantes para correspondência de padrões:

- Um ponto de exclamação (\!) no início da *charlist* significa que uma correspondência é feita se qualquer caractere, exceto aqueles em *charlist* , for encontrado na *expressão*. Quando utilizado fora dos colchetes, o ponto de exclamação faz sua própria correspondência.

- Você pode usar o hífen (-) no início (após um ponto de exclamação, se utilizado) ou no final da *charlist* para sua própria correspondência. Em outro local, o hífen identifica um intervalo de caracteres ANSI.

- Quando você especifica um intervalo de caracteres, os caracteres devem ser exibidos em ordem de classificação crescente (A-Z ou 0-100). \[A-Z\] é um padrão válido, mas \[Z-a\] não é.

- A sequência \[ \] de caracteres é ignorada; Ela é considerada como uma cadeia de caracteres de comprimento zero ("").

