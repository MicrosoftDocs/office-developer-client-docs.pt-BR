---
title: Propriedade Campo2. ValidationText (DAO)
TOCTitle: ValidationText Property
ms:assetid: 6128f66c-3891-ae4d-d12d-354a79a9c05e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194867(v=office.15)
ms:contentKeyID: 48545202
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4d58cb6bd32bd46b0a6bcec40ff68cdc52eebc31
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292619"
---
# <a name="field2validationtext-property-dao"></a>Propriedade Campo2. ValidationText (DAO)


**Aplica-se ao:** Access 2013, Office 2013

Define ou retorna um valor que especifica o texto da mensagem que o aplicativo exibe se o valor de um objeto **Field2** não atende à regra de validação especificada pela configuração da propriedade **ValidationRule** (apenas espaços de trabalho do Microsoft Access). **String** de leitura/gravação.

## <a name="syntax"></a>Sintaxe

*expressão* . ValidationText

*expressão* Uma variável que representa um objeto **campo2** .

## <a name="remarks"></a>Comentários

O valor de configuração ou de retorno é uma **String** que especifica o texto exibido se um usuário tenta digitar um valor inválido em um campo. Para um objeto que não está acrescentado a uma coleção, essa propriedade é de leitura/gravação.

Para um objeto **Field2**, a utilização da propriedade **ValidationText** depende do objeto que contém a coleção **[Fields](fields-collection-dao.md)** à qual o objeto **Field2** foi acrescentado, como mostra a tabela a seguir.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Objeto acrescentado a</p></th>
<th><p>Uso</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Índice</strong></p></td>
<td><p>Sem suporte</p></td>
</tr>
<tr class="even">
<td><p><strong>QueryDef</strong></p></td>
<td><p>Somente leitura</p></td>
</tr>
<tr class="odd">
<td><p><strong>Recordset</strong></p></td>
<td><p>Somente leitura</p></td>
</tr>
<tr class="even">
<td><p><strong>Relação</strong></p></td>
<td><p>Sem suporte</p></td>
</tr>
<tr class="odd">
<td><p><strong>TableDef</strong></p></td>
<td><p>Leitura/gravação</p></td>
</tr>
</tbody>
</table>

