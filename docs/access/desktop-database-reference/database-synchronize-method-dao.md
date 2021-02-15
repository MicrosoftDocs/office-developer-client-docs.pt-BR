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
localization_priority: Normal
ms.openlocfilehash: 411948f3c0ac4d6c353cd2722136dffb6a25fb17
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294705"
---
# <a name="databasesynchronize-method-dao"></a>Método Database.Synchronize (DAO)


**Aplica-se ao:** Access 2013, Office 2013

Sincroniza duas réplicas. (apenas espaços de trabalho do Microsoft Access).

## <a name="syntax"></a>Sintaxe

*expressão* . Synchronize(***DbPathName***, ***ExchangeType***)

*expressão* Uma variável que representa um objeto do **Banco de dados**.

## <a name="parameters"></a>Parâmetros

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
<th><p>Necessária/opcional</p></th>
<th><p>Tipo de dados</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>DbPathName</em></p></td>
<td><p>Obrigatório</p></td>
<td><p><strong>String</strong></p></td>
<td><p>O caminho para a réplica de destino com a qual o banco de dados será sincronizado.</p></td>
</tr>
<tr class="even">
<td><p><em>ExchangeType</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variantes</strong></p></td>
<td><p>Uma <strong><a href="synchronizetypeenum-enumeration-dao.md">constante SynchronizeTypeEnum</a></strong> que indica qual direção sincronizar as alterações entre os dois bancos de dados.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

Utilize **Synchronize** para trocar dados e alterações de design entre os dois bancos de dados. As alterações de design sempre ocorrem primeiro. Ambos os bancos de dados devem estar no mesmo nível de design antes de poderem trocar dados. Por exemplo, uma troca do tipo **dbRepExportChanges** pode causar alterações de design em uma réplica, mesmo que as alterações de dados fluam apenas do banco de dados para DbPathName.

A réplica identificada em DbPathName deve fazer parte do mesmo conjunto de réplicas. Se ambas as réplicas tiverem a mesma configuração da propriedade **ReplicaID** ou forem Estruturas-mestres para dois conjuntos diferentes de réplica, a sincronização falhará.

Ao sincronizar duas réplicas na Internet, você deve usar a constante **dbRepSyncInternet**. Nesse caso, especifique um endereço URL para o argumento DbPathName em vez de especificar um caminho de rede local.


> [!NOTE]
> [!OBSERVAçãO] Não é possível sincronizar réplicas parciais com outras réplicas parciais. Consulte o método [PopulatePartial](database-populatepartial-method-dao.md) para obter mais informações.


