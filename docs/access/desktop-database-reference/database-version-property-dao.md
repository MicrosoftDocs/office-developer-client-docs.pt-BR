---
title: Propriedade Database.Version (DAO)
TOCTitle: Version Property
ms:assetid: 40faaa0c-e764-e968-f606-7e06ded80c3f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192887(v=office.15)
ms:contentKeyID: 48544440
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4bcb360caa71131f4892409805c7afe3ceb2dcce
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25465304"
---
# <a name="databaseversion-property-dao"></a>Propriedade Database.Version (DAO)


**Aplica-se a**: Access 2013 | Office 2013

Em um espaço de trabalho do Microsoft Access , retorna a versão do mecanismo de banco de dados do Microsoft Jet ou do Microsoft Access que criou o banco de dados. **String** de somente leitura.

## <a name="syntax"></a>Sintaxe

*expressão* . Versão

*expressão* Uma variável que representa um objeto de **banco de dados** .

## <a name="remarks"></a>Comentários

O valor de retorno é uma cadeia de caracteres que avalia o número da versão, formatado como se segue.

  - O espaço de trabalho do Microsoft Access representa o número da versão na fórmula "*maior.menor*". Por exemplo, "3.0". O número da versão do produto é composto do número da versão (3), de um ponto e do número do lançamento (0).

A tabela a seguir mostra qual versão do mecanismo do banco de dados foi incluída nas várias versões dos produtos Microsoft.

<table style="width:100%;">
<colgroup>
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Mecanismo do Banco de Dados</p></th>
<th><p>Versão (ano do lançamento)</p></th>
<th><p>Microsoft Access</p></th>
<th><p>Microsoft Visual Basic</p></th>
<th><p>Microsoft Excel</p></th>
<th><p>Microsoft Visual C++</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Microsoft Jet</p></td>
<td><p>1.0 (1992)</p></td>
<td><p>1.0</p></td>
<td><p>N/D</p></td>
<td><p>N/A</p></td>
<td><p>N/D</p></td>
</tr>
<tr class="even">
<td><p>Microsoft Jet</p></td>
<td><p>1.1 (1993)</p></td>
<td><p>1.1</p></td>
<td><p>3.0</p></td>
<td><p>N/D</p></td>
<td><p>N/D</p></td>
</tr>
<tr class="odd">
<td><p>Microsoft Jet</p></td>
<td><p>2.0 (1994)</p></td>
<td><p>2.0</p></td>
<td><p>N/D</p></td>
<td><p>N/A</p></td>
<td><p>N/D</p></td>
</tr>
<tr class="even">
<td><p>Microsoft Jet</p></td>
<td><p>2.5 (1995)</p></td>
<td><p>N/D</p></td>
<td><p>4.0 (16 bits)</p></td>
<td><p>N/D</p></td>
<td><p>N/D</p></td>
</tr>
<tr class="odd">
<td><p>Microsoft Jet</p></td>
<td><p>3.0 (1995)</p></td>
<td><p>' 95 (7.0)</p></td>
<td><p>4.0 (32 bits)</p></td>
<td><p>' 95 (7.0)</p></td>
<td><p>4. x</p></td>
</tr>
<tr class="even">
<td><p>Microsoft Jet</p></td>
<td><p>3.5 (1996)</p></td>
<td><p>' 97 (8.0)</p></td>
<td><p>5.0</p></td>
<td><p>' 97 (8.0)</p></td>
<td><p>5.0</p></td>
</tr>
<tr class="odd">
<td><p>Microsoft Jet</p></td>
<td><p>4.0 (2000)</p></td>
<td><p>2000 (9.0)</p></td>
<td><p></p></td>
<td><p>2000 (9.0)</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Mecanismo do banco de dados do Microsoft Access</p></td>
<td><p>12.0 (2007)</p></td>
<td><p>2007</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>

