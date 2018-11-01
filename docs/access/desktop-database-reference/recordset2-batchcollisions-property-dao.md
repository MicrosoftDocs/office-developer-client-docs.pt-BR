---
title: Propriedade Recordset2.BatchCollisions (DAO)
TOCTitle: BatchCollisions Property
ms:assetid: 07d6c25f-baf5-f7d6-d225-0447e0f78fe6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844993(v=office.15)
ms:contentKeyID: 48543085
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1101180
f1_categories:
- Office.Version=v15
ms.openlocfilehash: ee26b84237b1bf4a8603295a6e6d66e6f30303e9
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25885887"
---
# <a name="recordset2batchcollisions-property-dao"></a>Propriedade Recordset2.BatchCollisions (DAO)


**Aplica-se a**: Access 2013, o Office 2013

## <a name="syntax"></a>Sintaxe

*expressão* . BatchCollisions

*expressão* Uma variável que representa um objeto **Recordset2** .

## <a name="remarks"></a>Comentários

Essa propriedade contém uma matriz de indicadores para as linhas que se encontram em colisão durante a última tentativa de chamada **[Update](recordset2-update-method-dao.md)** em lotes. A propriedade **[BatchCollisionCount](recordset2-batchcollisioncount-property-dao.md)** indica o número dos elementos na matriz.

Se você definir a propriedade [**Bookmark**](recordset2-bookmark-property-dao.md) do objeto **Recordset** em funcionamento como valores de indicador na matriz **BatchCollisions**, poderá mover cada registro com falha para concluir a operação de Atualização no modo de lotes mais recente.

Depois que os registros de colisão forem corrigidos, você poderá chamar o método **Update** do modo de lotes novamente. Nesse ponto, o DAO tentará outra atualização em lotes e a propriedade **BatchCollisions** refletirá novamente o conjunto de registros que falharam na segunda tentativa. Qualquer registro que foi bem-sucedido na tentativa anterior não será enviado para a tentativa atual porque agora possui a propriedade **[RecordStatus](recordset2-recordstatus-property-dao.md)** de dbRecordUnmodified. Esse processo poderá continuar enquanto ocorrem colisões ou até que você desista das atualizações e feche o conjunto de resultados.

Essa matriz é recriada sempre que você executar um método **Update** no modo em lote.

