---
title: Editando registros existentes
TOCTitle: Editing existing records
ms:assetid: 86b961e0-e0a5-85a2-1138-7ab2e696ec11
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249585(v=office.15)
ms:contentKeyID: 48546089
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 37da1e888eaa4231c58155e6830477f853b4027f
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944666"
---
# <a name="editing-existing-records"></a>Editando registros existentes


**Aplica-se a**: Access 2013, o Office 2013

Para editar registros existentes, vá para a linha que você deseja editar e altere a propriedade **Value** dos campos a serem alterados. Para obter mais informações sobre a propriedade **Value** do objeto **Field**, consulte o [Capítulo 3: Examinando dados](chapter-3-examining-data.md). Dependendo do tipo de cursor, você usará **Update** ou **UpdateBatch** para enviar alterações de volta para a fonte de dados. Para obter mais informações, consulte o [Capítulo 5: Atualizando e persistindo dados](chapter-5-updating-and-persisting-data.md).

Em geral, é mais eficiente usar um procedimento armazenado com um objeto de comando para realizar atualizações, bem como para executar outras operações, pois o procedimento armazenado não requer a criação de um cursor. Para obter mais informações sobre cursores, consulte o [Capítulo 8: Noções básicas sobre cursores e proteções](chapter-8-understanding-cursors-and-locks.md).

