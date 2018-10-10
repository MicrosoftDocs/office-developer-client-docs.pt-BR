---
title: FieldStatusEnum (referência de banco de dados da área de trabalho do Access)
TOCTitle: FieldStatusEnum
ms:assetid: 49570042-8435-8618-3ba1-7006c47735e0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249225(v=office.15)
ms:contentKeyID: 48544635
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e5c7ecb345c993b2582ce6971044d325afca857a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25465192"
---
# <a name="fieldstatusenum"></a>FieldStatusEnum


**Aplica-se a**: Access 2013 | Office 2013

Especifica o status de um objeto **Field**.

O valor **adFieldPending\*** indica a operação que causou a definição do status e pode ser combinado a outros valores de status.

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
<td><p><strong>adFieldAlreadyExists</strong></p></td>
<td><p>26</p></td>
<td><p>Indica que o campo especificado já existe.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldBadStatus</strong></p></td>
<td><p>12</p></td>
<td><p>Indica que um valor de status inválido foi enviado do ADO para o provedor de OLE DB. As possíveis causas incluem um provedor de OLE DB 1.0 ou 1.1, ou uma combinação inadequada de <a href="value-property-ado.md">Value</a> e <a href="status-property-ado-field.md">Status</a>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldCannotComplete</strong></p></td>
<td><p>20</p></td>
<td><p>Indica que o servidor da URL especificado por <a href="source-property-ado-record.md">Source</a> não pôde concluir a operação.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldCannotDeleteSource</strong></p></td>
<td><p>23</p></td>
<td><p>Indica que durante uma operação move, uma árvore ou subárvore foi movida para uma nova localização, mas a fonte não pôde ser excluída.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldCantConvertValue</strong></p></td>
<td><p>2</p></td>
<td><p>Indica que o campo não pode ser recuperado nem armazenado sem perda de dados.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldCantCreate</strong></p></td>
<td><p>7</p></td>
<td><p>Indica que o campo não pôde ser adicionado porque o provedor excedeu um limite (como o número permitido de campos).</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldDataOverflow</strong></p></td>
<td><p>6</p></td>
<td><p>Indica que os dados retornados do provedor sobrecarregaram o tipo de dados do campo.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldDefault</strong></p></td>
<td><p>13</p></td>
<td><p>Indica que o valor padrão do campo foi usado durante a definição dos dados.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldDoesNotExist</strong></p></td>
<td><p>16</p></td>
<td><p>Indica que o campo especificado não existe.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldIgnore</strong></p></td>
<td><p>15</p></td>
<td><p>Indica que esse campo foi ignorado quando os valores dos dados foram definidos na fonte. O provedor não definiu nenhum valor.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldIntegrityViolation</strong></p></td>
<td><p>10</p></td>
<td><p>Indica que não é possível modificar o campo porque ele é uma entidade calculada ou derivada.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldInvalidURL</strong></p></td>
<td><p>17</p></td>
<td><p>Indica que a URL da fonte de dados contém caracteres inválidos.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldIsNull</strong></p></td>
<td><p>3</p></td>
<td><p>Indica que o provedor retornou um valor VARIANT do tipo VT_NULL e que o campo não está vazio.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldOK</strong></p></td>
<td><p>0</p></td>
<td><p>Padrão. Indica que o campo foi adicionado ou excluído com sucesso.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldOutOfSpace</strong></p></td>
<td><p>22</p></td>
<td><p>Indica que o provedor não conseguiu obter espaço de repositório suficiente para concluir uma operação de movimentação ou cópia.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldPendingChange</strong></p></td>
<td><p>0x40000</p></td>
<td><p>Indica que o campo foi excluído e, em seguida, adicionado novamente, talvez com um tipo de dados diferente, ou que o valor do campo, que anteriormente tinha um status de adFieldOK, foi alterado. O formato final do campo modificará a coleção <a href="fields-collection-ado.md">Fields</a> depois que o método <a href="update-method-ado.md">Update</a> for chamado.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldPendingDelete</strong></p></td>
<td><p>0x20000</p></td>
<td><p>Indica que a operação <strong>Delete</strong> causou a definição do status. O campo foi marcado para ser excluído da coleção <strong>Fields</strong> depois que o método <strong>Update</strong> for chamado.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldPendingInsert</strong></p></td>
<td><p>0x10000</p></td>
<td><p>Indica que a operação <strong>Append</strong> causou a definição do status. <strong>Field</strong> foi marcado para ser adicionado à coleção <strong>Fields</strong> depois que o método <strong>Update</strong> for chamado.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldPendingUnknown</strong></p></td>
<td><p>0x80000</p></td>
<td><p>Indica que o provedor não pode determinar quais operações causaram a definição do status do campo.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldPendingUnknownDelete</strong></p></td>
<td><p>0x100000</p></td>
<td><p>Indica que o provedor não pode determinar qual operação causou a definição do status do campo e que o campo será excluído da coleção <strong>Fields</strong> depois que o método <strong>Update</strong> for chamado.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldPermissionDenied</strong></p></td>
<td><p>9</p></td>
<td><p>Indica que o campo não pode ser modificado porque ele está definido como somente-leitura.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldReadOnly</strong></p></td>
<td><p>24</p></td>
<td><p>Indica que o campo na fonte de dados está definido como somente-leitura.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldResourceExists</strong></p></td>
<td><p>19</p></td>
<td><p>Indica que o provedor não pôde executar a operação porque um objeto já existe na URL de destino e não é possível sobrescrevê-lo.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldResourceLocked</strong></p></td>
<td><p>18</p></td>
<td><p>Indica que o provedor não pôde executar a operação porque a fonte de dados está bloqueada por um ou mais aplicativos ou processos diferentes.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldResourceOutOfScope</strong></p></td>
<td><p>25</p></td>
<td><p>Indica que uma URL de origem ou de destino está fora do escopo do registro atual.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldSchemaViolation</strong></p></td>
<td><p>11</p></td>
<td><p>Indica que o valor violou a restrição do esquema da fonte de dados para o campo.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldSignMismatch</strong></p></td>
<td><p>5</p></td>
<td><p>Indica que o valor dos dados retornado pelo provedor estava assinado, mas o tipo de dados do valor do campo ADO não estava.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldTruncated</strong></p></td>
<td><p>4</p></td>
<td><p>Indica que os dados de comprimento variável estavam truncados durante a leitura a partir da fonte de dados.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldUnavailable</strong></p></td>
<td><p>8</p></td>
<td><p>Indica que o provedor não pôde determinar o valor durante a leitura da fonte de dados. Por exemplo, a linha acabou de ser criada, o valor padrão para a coluna não está disponível e um novo valor ainda não foi especificado.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldVolumeNotFound</strong></p></td>
<td><p>21</p></td>
<td><p>Indica que o provedor não pôde localizar o volume de repositório indicado pela URL.</p></td>
</tr>
</tbody>
</table>


**ADO/WFC Equivalente**

Essas constantes não têm ADO/WFC equivalentes.

