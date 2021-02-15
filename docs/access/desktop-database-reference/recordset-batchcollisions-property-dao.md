---
title: Propriedade Recordset.BatchCollisions (DAO)
TOCTitle: BatchCollisions Property
ms:assetid: 53e5572b-770c-9ea5-31a5-984abdf66faa
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194079(v=office.15)
ms:contentKeyID: 48544881
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 61f60567ac170a0ecde2d4bd46589d2308b7788f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300858"
---
# <a name="recordsetbatchcollisions-property-dao"></a>Propriedade Recordset.BatchCollisions (DAO)


**Aplica-se ao:** Access 2013, Office 2013

## <a name="syntax"></a>Sintaxe

*expressão* . BatchCollisions

*expression* Uma variável que representa um objeto **Recordset**.

## <a name="remarks"></a>Comentários

Essa propriedade contém uma matriz de indicadores para linhas que encontraram uma colisão durante a última tentativa de chamada de **[Update](recordset-update-method-dao.md)** em lote. A propriedade **[BatchCollisionCount](recordset-batchcollisioncount-property-dao.md)** indica o número de elementos na matriz.

Se você definir trabalhar com a propriedade **[Bookmark](recordset-object-dao.md)** do objeto **[Recordset](recordset-bookmark-property-dao.md)** para indicar valores na matriz **BatchCollisions**, poderá mover-se para cada registro com falha para concluir a operação de atualização mais recente no modo em lote.

Depois que os registros de colisão são corrigidos, você pode chamar novamente o método **Update** no modo em lote. Nesse momento, o DAO tenta outra atualização em lote, e a propriedade **BatchCollisions** reflete novamente o conjunto de registros que falharam na segunda tentativa. Os registros bem-sucedidos na tentativa anterior não são enviados para a tentativa atual, pois eles têm agora uma propriedade **[RecordStatus](recordset-recordstatus-property-dao.md)** de dbRecordUnmodified. Esse processo pode continuar até não haver mais colisões ou até você parar as atualizações e fechar a definição de resultados.

Essa matriz será recriada toda vez que for executado o método **Update** do modo de lotes.

