---
title: Propriedade Database.CollatingOrder (DAO)
TOCTitle: CollatingOrder Property
ms:assetid: 7f6c35bf-e5f9-8423-608e-bc072ca09141
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196459(v=office.15)
ms:contentKeyID: 48545901
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6101729af7f77e1451de240deece2bf789110fb7
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464490"
---
# <a name="databasecollatingorder-property-dao"></a>Propriedade Database.CollatingOrder (DAO)


**Aplica-se a**: Access 2013 | Office 2013

Retorna um valor que especifica a sequência da ordem de classificação no texto para comparação ou classificação da sequência (apenas espaços de trabalho do Microsoft Access). **Long** somente leitura.

## <a name="syntax"></a>Sintaxe

*expressão* . CollatingOrder

*expressão* Uma variável que representa um objeto de **banco de dados** .

## <a name="remarks"></a>Comentários

O valor de retorno é uma constante ou um valor **Long** que pode ser um dos valores a seguir.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constante</p></th>
<th><p>Ordem de classificação</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>dbSortGeneral</strong></p></td>
<td><p>Geral (inglês, francês, alemão, português, italiano e espanhol moderno)</p></td>
</tr>
<tr class="even">
<td><p><strong>dbSortArabic</strong></p></td>
<td><p>Árabe</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbSortChineseSimplified</strong></p></td>
<td><p>Chinês simplificado</p></td>
</tr>
<tr class="even">
<td><p><strong>dbSortChineseTraditional</strong></p></td>
<td><p>Chinês tradicional</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbSortCyrillic</strong></p></td>
<td><p>Russo</p></td>
</tr>
<tr class="even">
<td><p><strong>dbSortCzech</strong></p></td>
<td><p>Tcheco</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbSortDutch</strong></p></td>
<td><p>Holandês</p></td>
</tr>
<tr class="even">
<td><p><strong>dbSortGreek</strong></p></td>
<td><p>Grego</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbSortHebrew</strong></p></td>
<td><p>Hebraico</p></td>
</tr>
<tr class="even">
<td><p><strong>dbSortHungarian</strong></p></td>
<td><p>Húngaro</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbSortIcelandic</strong></p></td>
<td><p>Islandês</p></td>
</tr>
<tr class="even">
<td><p><strong>dbSortJapanese</strong></p></td>
<td><p>Japonês</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbSortKorean</strong></p></td>
<td><p>Coreano</p></td>
</tr>
<tr class="even">
<td><p><strong>dbSortNeutral</strong></p></td>
<td><p>Neutro</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbSortNorwDan</strong></p></td>
<td><p>Norueguês ou dinamarquês</p></td>
</tr>
<tr class="even">
<td><p><strong>dbSortPDXIntl</strong></p></td>
<td><p>Paradox International</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbSortPDXNor</strong></p></td>
<td><p>Paradox em norueguês ou dinamarquês</p></td>
</tr>
<tr class="even">
<td><p><strong>dbSortPDXSwe</strong></p></td>
<td><p>Paradox em sueco ou finlandês</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbSortPolish</strong></p></td>
<td><p>Polonês</p></td>
</tr>
<tr class="even">
<td><p><strong>dbSortSlovenian</strong></p></td>
<td><p>Esloveno</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbSortSpanish</strong></p></td>
<td><p>Espanhol</p></td>
</tr>
<tr class="even">
<td><p><strong>dbSortSwedFin</strong></p></td>
<td><p>Sueco ou finlandês</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbSortThai</strong></p></td>
<td><p>Tailandês</p></td>
</tr>
<tr class="even">
<td><p><strong>dbSortTurkish</strong></p></td>
<td><p>Turco</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbSortUndefined</strong></p></td>
<td><p>Indefinido ou desconhecido</p></td>
</tr>
</tbody>
</table>


A configuração da propriedade **CollatingOrder** corresponde ao argumento locale do método **CreateDatabase** quando o banco de dados foi criado ou o método **CompactDatabase** quando o banco de dados foi recentemente compactado.

Verifique a configuração da propriedade **CollatingOrder** de um objeto **Database** ou **Field** para determinar o método de comparação da sequência para o banco de dados ou o campo. Você pode definir a propriedade **CollatingOrder** de um objeto **Field** novo e não acrescentado se quiser que a configuração do objeto **Field** seja diferente da configuração do objeto **Database** que a contém.

