---
title: Método Database.Synchronize (DAO)
TOCTitle: Synchronize Method
ms:assetid: 5e716a4a-2430-8106-5c34-a02dd28bc4f6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194659(v=office.15)
ms:contentKeyID: 48545137
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053357
f1_categories:
- Office.Version=v15
ms.openlocfilehash: af280c1fca9465d9d8c02c2496ccc7b74e4d8b5d
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867514"
---
# <a name="databasesynchronize-method-dao"></a>Método Database.Synchronize (DAO)


**Aplica-se a**: Access 2013, o Office 2013

Sincroniza duas réplicas. (apenas espaços de trabalho do Microsoft Access).

## <a name="syntax"></a>Sintaxe

*expressão* . Sincronizar (***DbPathName***, ***ExchangeType***)

*expressão* Uma variável que representa um objeto de **banco de dados** .

### <a name="parameters"></a>Parâmetros

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nome</p></th>
<th><p>Obrigatório/Opcional</p></th>
<th><p>Tipo de dados</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>DbPathName</p></td>
<td><p>Obrigatório</p></td>
<td><p><strong>Cadeia de caracteres</strong></p></td>
<td><p>O caminho para a réplica de destino com a qual o banco de dados será sincronizado.</p></td>
</tr>
<tr class="even">
<td><p>ExchangeType</p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Uma constante <strong><a href="synchronizetypeenum-enumeration-dao.md">SynchronizeTypeEnum</a></strong> indicando a direção para sincronização das alterações entre os dois bancos de dados.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

Utilize **Synchronize** para trocar dados e alterações de design entre os dois bancos de dados. As alterações de design sempre ocorrem primeiro. Ambos os bancos de dados devem estar no mesmo nível de design antes de poderem trocar dados. Por exemplo, uma troca de tipo **dbRepExportChanges** pode causar alterações de design em uma réplica, mesmo que as alterações de dados fluxo apenas do banco de dados em DbPathName.

A réplica identificada no DbPathName deve fazer parte do mesmo conjunto de réplicas. Se ambas as réplicas tiverem a mesma configuração da propriedade **ReplicaID** ou forem Estruturas-mestres para dois conjuntos diferentes de réplica, a sincronização falhará.

Ao sincronizar duas réplicas na Internet, você deve usar a constante **dbRepSyncInternet**. Nesse caso, você pode especificar um endereço de Uniform Resource Locator (URL) para o argumento DbPathName em vez de especificar um caminho de rede local.


> [!NOTE]
> [!OBSERVAçãO] Não é possível sincronizar réplicas parciais com outras réplicas parciais. Consulte o método [PopulatePartial](database-populatepartial-method-dao.md) para obter mais informações.


