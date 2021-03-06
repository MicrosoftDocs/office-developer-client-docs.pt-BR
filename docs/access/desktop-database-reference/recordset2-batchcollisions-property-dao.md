---
title: Recordset2.Batpropriedade chCollisions (DAO)
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
localization_priority: Normal
ms.openlocfilehash: ea75da06c0db4eeb4e846bacfddc9f125c03fc84
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307487"
---
# <a name="recordset2batchcollisions-property-dao"></a>Recordset2.Batpropriedade chCollisions (DAO)


**Aplica-se ao:** Access 2013, Office 2013

## <a name="syntax"></a>Sintaxe

*expressão* . BatchCollisions

*expressão* Uma variável que representa **um objeto Recordset2** .

## <a name="remarks"></a>Comentários

Essa propriedade contém uma matriz de indicadores para as linhas que se encontram em colisão durante a última tentativa de chamada **[Update](recordset2-update-method-dao.md)** em lotes. A propriedade **[BatchCollisionCount](recordset2-batchcollisioncount-property-dao.md)** indica o número dos elementos na matriz.

Se você definir a propriedade [**Bookmark**](recordset2-bookmark-property-dao.md) do objeto **Recordset** em funcionamento como valores de indicador na matriz **BatchCollisions**, poderá mover cada registro com falha para concluir a operação de Atualização no modo de lotes mais recente.

Depois que os registros de colisão forem corrigidos, você poderá chamar o método **Update** do modo de lotes novamente. Nesse ponto, o DAO tentará outra atualização em lotes e a propriedade **BatchCollisions** refletirá novamente o conjunto de registros que falharam na segunda tentativa. Qualquer registro que foi bem-sucedido na tentativa anterior não será enviado para a tentativa atual porque agora possui a propriedade **[RecordStatus](recordset2-recordstatus-property-dao.md)** de dbRecordUnmodified. Esse processo poderá continuar enquanto ocorrem colisões ou até que você desista das atualizações e feche o conjunto de resultados.

Essa matriz será recriada toda vez que for executado o método **Update** do modo de lotes.

