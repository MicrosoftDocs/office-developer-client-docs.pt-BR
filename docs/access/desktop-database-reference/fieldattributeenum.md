---
title: FieldAttributeEnum (referência do banco de dados de área de trabalho do Access)
TOCTitle: FieldAttributeEnum
ms:assetid: 2d3a541e-a437-6108-ab0e-90c7884b3df7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249071(v=office.15)
ms:contentKeyID: 48543967
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 079c79af3d15a6a5864a7db7f8334393258cfd42
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292598"
---
# <a name="fieldattributeenum"></a>FieldAttributeEnum

**Aplica-se ao:** Access 2013, Office 2013

Especifica um ou mais atributos de um objeto [Field](field-object-ado.md).

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constant</p></th>
<th><p>Valor</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adFldCacheDeferred</strong></p></td>
<td><p>0x1000</p></td>
<td><p>Indica que o provedor armazena os valores do campo e que as leituras subsequentes são feitas do cache.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFldFixed</strong></p></td>
<td><p>0x10</p></td>
<td><p>Indica que o campo contém dados com tamanho fixo.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFldIsChapter</strong></p></td>
<td><p>0x2000</p></td>
<td><p>Indica que o campo contém um valor de capítulo que especifica um recordset filho para esse campo pai. Normalmente os campos de capítulo são usados com data shaping ou filtros.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFldIsCollection</strong></p></td>
<td><p>0x40000</p></td>
<td><p>Indica que o campo especifica que o recurso representado pelo registro é uma coleção de outros recursos, como pasta, em vez de um recurso simples, como arquivo de texto.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFldIsDefaultStream</strong></p></td>
<td><p>0x20000</p></td>
<td><p>Indica que o campo contém o fluxo padrão para o recurso representado pelo registro. Por exemplo, o Stream padrão pode ser o conteúdo HTML de uma pasta raiz em um site, que é automaticamente fornecido quando a URL raiz é especificada.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFldIsNullable</strong></p></td>
<td><p>0x20</p></td>
<td><p>Indica que o campo aceita os valores nulos.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFldIsRowURL</strong></p></td>
<td><p>0x10000</p></td>
<td><p>Indica que o campo contém a URL que nomeia o recurso do repositório de dados representado pelo registro.</p></td>
</tr>
<tr class="even">
<td><p><strong>Bit adfldlong</strong></p></td>
<td><p>0x80</p></td>
<td><p>Indica que o campo é campo binário longo. Além disso, indica que você pode utilizar os métodos <a href="appendchunk-method-ado.md">AppendChunk</a> e <a href="getchunk-method-ado.md">GetChunk</a>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFldMayBeNull</strong></p></td>
<td><p>0x40</p></td>
<td><p>Indica que você pode ler valores nulos do campo.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFldMayDefer</strong></p></td>
<td><p>0x2</p></td>
<td><p>Indica que o campo é adiado — isto é, os valores do campo não são recuperados da fonte de dados com todo o registro, mas somente quando você os acessa explicitamente.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFldNegativeScale</strong></p></td>
<td><p>0x4000</p></td>
<td><p>Indica que o campo representa um valor numérico de uma coluna que permite valores de escala negativos. A escala é especificada pela propriedade <a href="numericscale-property-ado.md">NumericScale</a>.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFldRowID</strong></p></td>
<td><p>0x100</p></td>
<td><p>Indica que o campo contém um identificador de linha persistente que não pode ser escrito e não tem nenhum valor significativo exceto o de identificar a linha (como um número de registro, identificador exclusivo e assim por diante).</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFldRowVersion</strong></p></td>
<td><p>0x200</p></td>
<td><p>Indica que o campo contém algum tipo de marcação de data e hora utilizada para controlar as atualizações.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFldUnknownUpdatable</strong></p></td>
<td><p>0x8</p></td>
<td><p>Indica que o provedor não pode determinar se você pode escrever no campo.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFldUnspecified</strong></p></td>
<td><p>-1<br />
0xFFFFFFFF</p></td>
<td><p>Indica que o provedor não especifica atributos de campo.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFldUpdatable</strong></p></td>
<td><p>0x4</p></td>
<td><p>Indica que você pode escrever no campo.</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>Equivalente do ADO/WFC

Pacote: **com.ms.wfc.data**

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constant</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>AdoEnums. Fieldattribute. CACHEDEFERRED</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. Fieldattribute. FIXED</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums. Fieldattribute. isNULLable</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. Fieldattribute. LONG</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums. Fieldattribute. MAYBENULL</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. Fieldattribute. MAYDEFER</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums. Fieldattribute. NEGATIVESCALE</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. Fieldattribute. ROWID</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums. Fieldattribute. doVERSION</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. Fieldattribute. UNKNOWNUPDATABLE</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums. Fieldattribute. unESPECIFICADO</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. Fieldattribute. ATUALIZável</p></td>
</tr>
</tbody>
</table>

