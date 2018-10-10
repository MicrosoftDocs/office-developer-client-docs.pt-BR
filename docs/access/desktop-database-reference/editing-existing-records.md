---
title: Editando registros existentes
TOCTitle: Editing Existing Records
ms:assetid: 86b961e0-e0a5-85a2-1138-7ab2e696ec11
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249585(v=office.15)
ms:contentKeyID: 48546089
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 274cd7667506159e2309fffb3596781c004f7006
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463841"
---
# <a name="editing-existing-records"></a>Editando registros existentes


**Aplica-se a**: Access 2013 | Office 2013

Para editar registros existentes, vá para a linha que você deseja editar e altere a propriedade **Value** dos campos a serem alterados. Para obter mais informações sobre a propriedade **Value** do objeto **Field**, consulte o [Capítulo 3: Examinando dados](chapter-3-examining-data.md). Dependendo do tipo de cursor, você usará **Update** ou **UpdateBatch** para enviar alterações de volta para a fonte de dados. Para obter mais informações, consulte o [Capítulo 5: Atualizando e persistindo dados](chapter-5-updating-and-persisting-data.md).

Em geral, é mais eficiente usar um procedimento armazenado com um objeto de comando para realizar atualizações, bem como para executar outras operações, pois o procedimento armazenado não requer a criação de um cursor. Para obter mais informações sobre cursores, consulte o [Capítulo 8: Noções básicas sobre cursores e proteções](chapter-8-understanding-cursors-and-locks.md).

